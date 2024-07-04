---
description: >-
  Making sense of how to organize import files (genomic and clinical) for
  cBioPortal project imports
---

# File Formats

The following table is organized by: the type of genomic data, its required format (also cBioPortal suggested filename convention - the link provided directs users to the specific section in the official [cBioPortal.org's documentation website](https://docs.cbioportal.org/5.1-data-loading/data-loading/file-formats#formats)), comments, and the mandatory associated meta file for the data file. For every data file in the import directory, there must be a meta file for it.

To setup and create a "minimal" cBioPortal project, you will need the following files:

* [meta\_study.txt](https://docs.cbioportal.org/file-formats/#meta-file)
* [meta\_clinical\_samples.txt](https://docs.cbioportal.org/file-formats/#meta-files)
* [data\_clinical\_samples.txt](https://docs.cbioportal.org/file-formats/#clinical-sample-columns)
* [case\_lists/](https://docs.cbioportal.org/file-formats/#case-lists)
  * [cases\_sequenced.txt](https://docs.cbioportal.org/file-formats/#required-case-lists)

**NOTE**: The more data that is provided, the better your project will be, and will be able to use cBioPortal's features. Creating a project with the bare minimal data will not be very useful to the user.

{% hint style="danger" %}
#### Please use _consistent sample IDs_ across all files (genomic and clinical files) – watch out for underscores and dashes!
{% endhint %}

### Data Types Summary Table

<table><thead><tr><th>Platform (data type)</th><th width="225">Required format</th><th width="210">Alternate formats</th><th width="241">Notes</th><th>Associated meta file</th></tr></thead><tbody><tr><td>Clinical (Sample centric)</td><td><a href="https://docs.cbioportal.org/5.1-data-loading/data-loading/file-formats#clinical-sample-columns">data_clinical<em>_</em>samples.txt</a></td><td></td><td>Samples file is mandatory; this file is where the mapping of the sample IDs happen (all sample IDs across all files, genomic and clinical files)</td><td>meta_clinical_samples.txt</td></tr><tr><td>Clinical (Patient centric)</td><td><a href="https://docs.cbioportal.org/5.1-data-loading/data-loading/file-formats#clinical-data">data_clinical<em>_</em>patients.txt</a></td><td></td><td></td><td>meta_clinical_patients.txt</td></tr><tr><td>WGS (SNV/Indels)</td><td><a href="https://docs.cbioportal.org/5.1-data-loading/data-loading/file-formats#mutation-data">data_mutations_extended.txt</a></td><td></td><td>Must be in MAF format; Run <a href="https://github.com/mskcc/vcf2maf">vcf2maf</a></td><td>meta_mutations_extended.txt</td></tr><tr><td>WGS (Structural Variants)</td><td><a href="https://docs.cbioportal.org/5.1-data-loading/data-loading/file-formats#structural-variant-data">data_sv.txt</a></td><td><a href="http://mavis.bcgsc.ca/docs/latest/mavis.summary.html?highlight=output">mavis_summary_*.tab file</a></td><td>cBioportal is still working on this; if you have fusions file instead, its fine</td><td>meta_sv.txt</td></tr><tr><td>RNA-Seq (Expression)</td><td><a href="https://docs.cbioportal.org/5.1-data-loading/data-loading/file-formats#expression-data">data_expressions.txt</a></td><td></td><td></td><td>meta_expressions.txt</td></tr><tr><td>RNA-Seq (Fusion)</td><td><a href="https://docs.cbioportal.org/5.1-data-loading/data-loading/file-formats#fusion-data">data_fusions.txt</a></td><td><a href="http://mavis.bcgsc.ca/docs/latest/mavis.summary.html?highlight=output">mavis_summary_*.tab file</a></td><td></td><td>meta_fusions.txt</td></tr><tr><td>Segmented (Seg)</td><td><a href="https://docs.cbioportal.org/5.1-data-loading/data-loading/file-formats#segmented-data">data_segments.seg</a></td><td></td><td></td><td>meta_segments.txt</td></tr><tr><td>Discrete Copy Number (CNA)</td><td><a href="https://docs.cbioportal.org/5.1-data-loading/data-loading/file-formats#discrete-copy-number-data">data_CNA.txt</a></td><td></td><td></td><td>meta_CNA.txt</td></tr><tr><td>Methylation</td><td><a href="https://docs.cbioportal.org/5.1-data-loading/data-loading/file-formats#methylation-data">data_methylation.txt</a></td><td></td><td></td><td>meta_methylation.txt</td></tr><tr><td>Protein (RPPA/Mass Spectrometry)</td><td><a href="https://docs.cbioportal.org/5.1-data-loading/data-loading/file-formats#protein-level-data">protein data</a></td><td>data_protein_quantification.txt</td><td>Depends if you have RPPA or Mass Spectrometry data; Log2value or z-score datatypes</td><td>meta_protein_quantification.txt</td></tr><tr><td></td><td></td><td>data_protein_quantification_Zscores.txt</td><td></td><td>meta_protein_quantification_Zscores.txt</td></tr><tr><td></td><td></td><td>data_rppa.txt</td><td></td><td>meta_rppa.txt</td></tr><tr><td></td><td></td><td>data_rppa_Zscores.txt</td><td></td><td>meta_rppa_Zscores.txt</td></tr><tr><td></td><td></td><td><a href="https://docs.cbioportal.org/5.1-data-loading/data-loading/file-formats#generic-assay">data_phosphoprotein_quantification.txt</a></td><td></td><td>meta_phosphoprotein_quantification.txt</td></tr><tr><td><a href="https://docs.cbioportal.org/5.1-data-loading/data-loading/file-formats">Other formats</a></td><td></td><td></td><td></td><td></td></tr></tbody></table>

{% hint style="warning" %}
**A samples file (aka data\_clinical\_samples.txt) is mandatory for a project import! It is the key file in mapping of the project's IDs.**&#x20;
{% endhint %}

### Skeleton of the directory structure

<figure><img src="../.gitbook/assets/skeleton_directory_structure.png" alt=""><figcaption><p>An example of how a directory of import files would look like</p></figcaption></figure>

{% hint style="info" %}
For more information on what the case\_list directory is and what case files are, please refer to the [Case List Files section](case-lists-files.md)
{% endhint %}
