*Example content from a bioinformatics SOP outlining the procedure for assessing the quality of Illumina sequencing data prior to downstream bioinformatics analyses.*

```{raw} html
<hr />
```

**Data Type & Analysis Selection**

This procedure is designed to process 150bp paired-end FASTQ files generated using Illumina sequencing platforms (e.g. MiSeq, NextSeq). Each sample should have two FASTQ files (.fastq or .fastq.gz) representing the forward and reverse reads.

The QC pipeline is specifically optimised and validated to process this data type and read length. Samples generated using other sequencing technologies (e.g. Oxford Nanopore, PacBio) or read lengths are not validated for analysis using this procedure.

The input data should be derived from microbial samples ; this procedure is not designed or validated for human sequencing datasets. Samples containing high levels of human derived reads will not pass QC thresholds. Analysis tools and pipeline parameters have been selected to align with the anticipated characteristics of microbial data.
