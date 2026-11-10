*Example content from a bioinformatics SOP outlining the procedure for assessing the quality of Illumina sequencing data prior to downstream bioinformatics analyses.*

```{raw} html
<hr />
```

**Procedure**

**1. Receipt of sequencing files**

Sequencing files are automatically imported onto the staging server upon completion of an Illumina sequencing run. The bioinformatics production server checks the staging server for completed runs every 10 minutes via a scheduled cron job. When a new completed run is detected, the production server automatically imports the files from the staging server to `/mnt/data/raw/<SEQUENCER_ID>/<RUN_ID>/` and initiates the bioinformatics QC pipeline, which is implemented in Nextflow and maintained at [https://github.com/lab-bioinformatics/qc-pipeline](https://github.com/lab-bioinformatics/qc-pipeline).

```{raw} html
<hr>
```

**2. Executing the analysis**

The bioinformatics QC pipeline can be executed in two modes:

1. **Automated Mode:** The pipeline is launched automatically via a cron job when a new sequencing run is copied from the staging server.
2. **Manual Mode:** A user can manually initiate the pipeline on a selected set of FASTQ files.

**2.1 Manually launching the pipeline**

:::{note}
Manual mode should only be used where a run has failed because of a server issue (e.g. a power cut that stopped the analysis part way through). Manual mode can only be initiated by a member of the bioinformatics team as access to servers is restricted.
:::

To restart a failed run:

Log into the production server using an ssh client and switch to a user profile with appropriate permissions:

```bash
ssh username@10.0.1.12
sudo su - prod-user
```

Access to the server is restricted and can only be made from within the laboratory network. Users must either be connected via a wired network connection or have an active VPN session to reach the server.

If the samples were sequenced in-house, navigate to the directory for the relevant sequencing run by changing into the appropriate path, for example:

```bash cd /mnt/data/raw/<SEQUENCER_ID>/<RUN_ID>/Data/Intensities/BaseCalls/

```

Once in the directory, verify that FASTQ files are present by listing them:

```bash ls *.fastq.qz

```

This command will display all FASTQ files in the directory. If no FASTQ files are found, first check whether the sequencing run has completed. If the run has finished and no FASTQ files are present, the sequencing run or the file transfer may have failed. In this case, refer to **SOP045: Using the NextSeq 550 for further guidance**.

If FASTQ files are present for all expected samples within a run, you are ready to run the QC pipeline on them. To manually initiate the bioinformatics QC pipeline on the FASTQ files, run the following command from within the run-level directory:

```bash nextflow run /path/to/qc_pipeline.nf \     --input /mnt/data/raw/<SEQUENCER_ID>/<RUN_ID> \     -profile prod,slurm

```

The QC pipeline will now be submitted to the production job queue. Because Nextflow launches one Slurm job per process (or per task if parallelised), multiple jobs will appear in the queue. The status of these jobs can be monitored using:

> ```bash squeue -u prod-user
>
> ```

Once sufficient compute resources become available, the job scheduler will start the pipeline. The scheduler is configured so that jobs allocated to the production queue are prioritised; therefore, the QC pipeline should normally commence within a few minutes, depending on resource availability.

```{raw} html
<hr>
```

**3. Pipeline overview**

The bioinformatics QC pipeline completes the following steps:

> 01. FASTQ files are paired based on their name using pattern matching to identify which samples are “forward” and which are “reverse”.
> 02. The workstream associated with each pair of FASTQ files is identified based on the sample name (e.g. FLU for the flu workstream, SARS for the SARS CoV 2 workstream).
> 03. Metadata including run ID, flowcell ID, and instrument ID are extracted from FASTQ files.
> 04. A check is performed to determine whether a directory for that run already exists within the relevant workstream folder (e.g. `/mnt/data/analysis/flu/<RUN_ID>/`); if not, one is created.
> 05. A backup copy of the raw sequencing data is created on cold storage (`/mnt/archive/raw/<SEQUENCER_ID>/<RUN_ID>/`).
> 06. Cutadapt and FastQC (via the Trim Galore! wrapper) are run, producing trimmed FASTQ files and QC reports, which are stored in the qc subfolder.
> 07. The trimmed FASTQ files are screened using Centrifuge against a reference database of human, bacterial, viral, and archaeal genomes.
> 08. A graphical representation of sample content is generated using Krona, based on Centrifuge output.
> 09. All QC outputs (from Cutadapt and FastQC) are collated into a single report using MultiQC (`/mnt/data/analysis/<WORKSTREAM>/<RUN_ID>/qc/multiqc/`).
> 10. Run level and per sample entries are created in the AutoQC database.

Once the analysis has completed, results are written to workstream specific subdirectories under the qc folder: `/mnt/data/analysis/<WORKSTREAM>/<RUN_ID>/qc`. Within this directory, the following subdirectories are generated:

**MultiQC Report**

`/mnt/data/analysis/<WORKSTREAM>/<RUN_ID>/qc/multiqc/`

Contains the consolidated QC summary (multiqc_report.html), which collates metrics across all workstream specific sequencing files processed in the run.

**Trimmed Reads**

`/mnt/data/analysis/<WORKSTREAM>/<RUN_ID>/qc/trimmed_reads/`

Contains adapter trimmed FASTQ files. These cleaned reads are suitable for downstream analyses such as alignment, variant calling, or further project specific workflows.

**Centrifuge Report**

`/mnt/data/analysis/<WORKSTREAM>/<RUN_ID>/qc/centrifuge/`

Contains a graphic report summarising the species assignments of reads that could be classified using Centrifuge.

```{raw} html
<hr>
```

**4. Checking samples have passed QC**

Once the QC pipeline has completed, the final step is to verify whether each sample has met the laboratory’s minimum quality standards. While the pipeline writes result files to `/mnt/data/analysis/<WORKSTREAM>/<RUN_ID>/qc/`, this verification is performed through the AutoQC database, which collates and stores QC metrics for every sequencing run. The database acts as a gatekeeper for downstream bioinformatics workflows, ensuring that only samples which pass QC thresholds are released for further analysis.

**4.1 Accessing the AutoQC database**

The AutoQC database is hosted on the laboratory’s datastore and can be accessed through a secure IP address. Access is restricted to connections made from within the laboratory’s internal network or via an approved VPN session. To connect, open a web browser and navigate to: `http://10.0.2.25/autoqc`.

Once the login page is displayed, enter your assigned user credentials to access the database. After logging in, the duty bioinformatician must review the QC status of all samples associated with the sequencing run. AutoQC automatically applies pass or fail flags based on predefined quality thresholds, including read depth, base quality scores, adapter contamination, and the proportion of human reads detected. Samples that meet all thresholds are marked as **QC Pass** and require no further action.

**4.2 Assessment of failed runs / samples**

For samples flagged as **QC Fail**, the duty bioinformatician is responsible for examining the detailed QC metrics to confirm the reason for failure. This involves reviewing outputs from MultiQC and Centrifuge to check whether project specific QC thresholds (Appendix 1) have been met. A sample is considered to have failed if:

> - The magnitude of reads assigned to the expected organism is lower than the minimum threshold specified for that project sample type (Appendix 2).
> - The average read length post trimming is shorter than 150 bp.
> - The per base N content exceeds 0.5%.
> - The average per base quality is lower than Q30 for the first 150 bp of the reads.

**4.3 Gatekeeping mechanism**

AutoQC functions as a gatekeeper by controlling the release of samples into downstream workflows. Only those marked as **QC Pass** are added to the whitelist for further bioinformatics processing, while failed samples are held back automatically. This mechanism ensures that downstream analysis is initiated exclusively on validated, high quality datasets, maintaining the integrity of laboratory outputs and preventing wasted compute resources.

**4.4 Escalation of QC failures**

In addition to database annotation, the duty bioinformatician must notify the wider laboratory team when a run contains failed samples. This is achieved by sending a message on Slack to the “sequencing” channel, summarising the run ID, the number of failed samples, and the reasons for failure. This communication ensures that sequencing staff within the laboratory can promptly take corrective action, such as scheduling resequencing or investigating potential problems with library preparation or instrument performance.
