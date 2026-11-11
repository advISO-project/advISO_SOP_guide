*Example content from a bioinformatics SOP outlining the procedure for assessing the quality of Illumina sequencing data prior to downstream bioinformatics analyses.*

```{raw} html
<hr />
```

**Resources & Tools**

The following equipment and software are required to perform quality control of sequencing datasets:

**Hardware:**

> - PC or equivalent workstation capable of accessing the laboratory’s production server.

**Software:**

> - SSH client software (e.g. PuTTY, Windows Subsytem for Linux, MobaXterm, etc.) for connecting to the laboratory’s production server and datastore.
> - Production version of the QC pipeline installed and configured on the production server.
> - Web browser for accessing the AutoQC database (<http://10.0.2.25/autoqc>).

**Network access:**

> - Access to the laboratory’s network with the sequencing server mapped as a network drive.
> - User account with adequate permissions to read/write sequencing data and QC outputs.

**Databases:**

> - Active user account on the AutoQC database, with bioinformatician-level authorisation to review QC metrics, record explanatory notes, and manage sample pass/fail status.
