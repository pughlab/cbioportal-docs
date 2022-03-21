---
description: Common Genomic files imported into cBioportal and their expected headers
---

# Common Genomic Headers

Most common genomic files imported are the mutations, fusion, seg, and CNA files. If the mutations data is run with vcf2maf, then having the expected cBioportal file headers are not to be of concern. The mutations (MAF) file can be also be created, please refer to the [cBioportal documentation](https://docs.cbioportal.org/5.1-data-loading/data-loading/file-formats#minimal-maf-format) for the details. It is highly recommended to run your mutations file through vcf2maf, as we would like all our project data to be consistent. The following file headers are for fusion, seg and CNA files, as users often want to know what they are.

## Fusion File

A [fusion data](https://docs.cbioportal.org/5.1-data-loading/data-loading/file-formats#fusion-data) file consists of one gene per row. It is a tab-delimited file, where the naming format and order of the headers must be the following:

| Hugo\_Symbol | Entrez\_Gene\_Id | Center | Tumor\_Sample\_Barcode | Fusion | DNA\_support | RNA\_support | Method | Frame |
| ------------ | ---------------- | ------ | ---------------------- | ------ | ------------ | ------------ | ------ | ----- |
|              |                  |        |                        |        |              |              |        |       |
|              |                  |        |                        |        |              |              |        |       |
|              |                  |        |                        |        |              |              |        |       |

* **Hugo\_Symbol**: A [HUGO](https://www.genenames.org) gene symbol (aka HGNC Hugo Gene Nomenclature Committee)
* **Entrez\_Gene\_Id**: A [Entrez Gene](https://www.ncbi.nlm.nih.gov/gene) identifier
* **Center**: The sequencing centre (eg UHN)
* **Tumor\_Sample\_Barcode**: This is the sample ID
* **Fusion**: A description of the fusion, e.g., "TMPRSS2-ERG fusion"
* **DNA\_support**: Fusion detected from DNA sequence data, values: "yes" or "no"
* **RNA\_support**: Fusion detected from RNA sequence data, values: "yes" or "no"
* **Method**: Fusion detected algorithm/tool
* **Frame**: "in-frame" or "frameshift"
* **Annotation (OPTIONAL)**:&#x20;
* **Fusion\_Status (OPTIONAL)**: An assessment of the mutation type (i.e., "SOMATIC", "GERMLINE", "UNKNOWN", or empty)

## Segmented File

A [segmented data](https://docs.cbioportal.org/5.1-data-loading/data-loading/file-formats#segmented-data) file (aka seg file) is a tab-delimited text file that lists loci and associated numeric values. When the seg data is imported, it enables the 'CNA' track on cBioPortal's Patient view within the Summary tab. The naming format and order of the headers must be the following:

| ID | chrom | loc.start | loc.end | num.mark | seg.mean |
| -- | ----- | --------- | ------- | -------- | -------- |
|    |       |           |         |          |          |
|    |       |           |         |          |          |
|    |       |           |         |          |          |

* **ID**: This is the sample ID
* **chrom**: Chromosome number; integer values only (no 'chr')
* **loc.start**: start location
* **loc.end**: end location
* **num.mark**: numeric value for that locus
* **seg.mean**: the mean

## CNA File

Copy Number Alteration Data (aka CNA file) can be displayed via two datatype methods on cBioPortal: [Discrete](https://docs.cbioportal.org/5.1-data-loading/data-loading/file-formats#discrete-copy-number-data) or [Continuous](https://docs.cbioportal.org/5.1-data-loading/data-loading/file-formats#continuous-copy-number-data) datatype. Please refer to the official cBioPortal's documentation for more details (provided in the links within datatype names). Either datatypes, the expected file format is a tab-delimited file, and consists of one gene per row and a sample per column (using the sample ID as the column header).

| Hugo\_Symbol | SAMPLE\_ID1 | SAMPLE\_ID2 | SAMPLE\_ID3 |
| ------------ | ----------- | ----------- | ----------- |
|              |             |             |             |
|              |             |             |             |
|              |             |             |             |



