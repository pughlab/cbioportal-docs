# Common Genomic Headers

Most common genomic files imported are the mutations, fusion, seg, and CNA files. If the mutations data is run with vcf2maf, then having the expected cBioportal file headers are not to be of concern. The mutations (MAF) file can be also be created, please refer to the [cBioportal documentation](https://docs.cbioportal.org/5.1-data-loading/data-loading/file-formats#minimal-maf-format) for the details. It is highly recommended to run your mutations file through vcf2maf, as we would like all our project data to be consistent. The following file headers are for fusion, seg and CNA files, as users often want to know what they are.

## Fusion File Headers

| Hugo\_Symbol | Entrez\_Gene\_Id | Center | Tumor\_Sample\_Barcode | Fusion | DNA\_support | RNA\_support | Method | Frame | Annotation |
| ------------ | ---------------- | ------ | ---------------------- | ------ | ------------ | ------------ | ------ | ----- | ---------- |
|              |                  |        |                        |        |              |              |        |       |            |
|              |                  |        |                        |        |              |              |        |       |            |
|              |                  |        |                        |        |              |              |        |       |            |

## Seg File Headers

| ID | chrom | loc.start | loc.end | num.mark | seg.mean |
| -- | ----- | --------- | ------- | -------- | -------- |
|    |       |           |         |          |          |
|    |       |           |         |          |          |
|    |       |           |         |          |          |

## CNA File Headers

| Hugo\_Symbol | SAMPLE\_ID1 | SAMPLE\_ID2 | SAMPLE\_ID3 |
| ------------ | ----------- | ----------- | ----------- |
|              |             |             |             |
|              |             |             |             |
|              |             |             |             |



