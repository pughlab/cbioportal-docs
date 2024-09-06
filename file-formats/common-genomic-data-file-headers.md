---
description: Common Genomic files imported into cBioportal and their expected headers
---

# Common Genomic Data File Headers

Most common genomic files imported are the mutations, fusion, seg, and CNA files. The following file headers are for fusion, seg and CNA files, as users often want to know what they are.

## Mutation File

The expected mutation file format cBioPortal expects upon project import is a [MAF](https://docs.gdc.cancer.gov/Data/File\_Formats/MAF\_Format/) file format. If the mutations data is run with [vcf2maf](https://github.com/mskcc/vcf2maf) with [Ensembl's VEP](http://useast.ensembl.org/info/docs/tools/vep/index.html), then having the expected cBioportal file headers and content are not to be of a concern. The [NIH GDC's MAF](https://docs.gdc.cancer.gov/Data/File\_Formats/MAF\_Format/#protected-maf-file-structure) file formats webpage provides details on what is each column and their definitions.

#### Deciding to create your own minimal MAF file

A minimal MAF file can be created and cBioPortal does accept a MAF with a minimal set of just four column headers for project import. For more information, please refer to the _minimal MAF format_ section of the [cBioportal documentation](https://docs.cbioportal.org/5.1-data-loading/data-loading/file-formats#minimal-maf-format) for the details.&#x20;

<table><thead><tr><th>Hugo_Symbol</th><th>Variant_Classification</th><th width="224">Tumor_Sample_Barcode</th><th>HGVSp_Short</th></tr></thead><tbody><tr><td>PPOX</td><td>Missense_Mutation</td><td>ABC-001-0001-AA</td><td>p.R168H</td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr></tbody></table>

* **Hugo\_Symbol**: A [HUGO](https://www.genenames.org/) gene symbol (aka HGNC Hugo Gene Nomenclature Committee)
* **Variant\_Classification**: A particular type of mutation. Acceptable values: `Frame_Shift_Del, Frame_Shift_Ins, In_Frame_Del, In_Frame_Ins, Missense_Mutation, Nonsense_Mutation, Silent, Splice_Site, Translation_Start_Site, Nonstop_Mutation, 3'UTR, 3'Flank, 5'UTR, 5'Flank, IGR, Intron, RNA, Targeted_Region, De_novo_Start_InFrame, De_novo_Start_OutOfFrame`. cBioPortal skips the following types during the import: `Silent, Intron, 3'UTR, 3'Flank, 5'UTR, 5'Flank, IGR and RNA`. Two extra values are allowed by cBioPortal here as well: `Splice_Region, Unknown`. ⚠️ the values should be in the correct case. E.g. `missense_mutation` is not allowed, while `Missense_Mutation` is.&#x20;
* **Tumor\_Sample**_**\_**_**Barcode**: This is the sample ID
* **HGVSp\_Short**: Protein change, e.g., p.T790M
  * <mark style="color:red;">NOTE</mark>: Please be aware that no 3-letter codes are allowed anymore.  \
    E.g. `p.Gly12Asp` <- instead it should be `p.G12D`
    * When p.G12D is used, then cBioportal can properly generate the mutation lollipop plot

#### Creating an extended MAF file

From a minimal MAF file, the next step to proceed in creating an extended MAF file would be to run the data in the [Genome Nexus Annotation Pipeline](https://github.com/genome-nexus/genome-nexus-annotation-pipeline). This pipeline will annotate variants to the [Genome Nexus Server](https://genomenexus.org/), and uses [Ensembl's VEP](http://useast.ensembl.org/info/docs/tools/vep/index.html) and it will select a single effect per variant.&#x20;

\
\* It is highly recommended to run your mutations file through vcf2maf, as we would like all our project data to be consistent.

## Structural Variant File

A [structural variant](https://docs.cbioportal.org/file-formats/#structural-variant-data) file is a tab-delimited file with one structural variant per row. It minimally requires a few headers: `Sample_Id`, either `Site1_Hugo_Symbol`/ `Site1_Entrez_Gene_Id` or `Site2_Hugo_Symbol`/ `Site2_Entrez_Gene_Id` and `SV_Status`

Additional annotation columns can be added to the structural variant file. From the official cBioportal documentation, they provide [a set of suggested field names](https://docs.cbioportal.org/file-formats/#data-file-9), permissible values and example values, please refer to their website.

## Segmented File

A [segmented data](https://docs.cbioportal.org/5.1-data-loading/data-loading/file-formats#segmented-data) file (aka seg file) is a tab-delimited text file that lists loci and associated numeric values. When the seg data is imported, it enables the 'CNA' track on cBioPortal's Patient view within the Summary tab. The naming format and order of the headers must be the following:

<table><thead><tr><th width="245">ID</th><th width="150">chrom</th><th>loc.start</th><th>loc.end</th><th>num.mark</th><th>seg.mean</th></tr></thead><tbody><tr><td>ABC-001-0001-AA</td><td>1</td><td>1629333</td><td>1654148</td><td>60</td><td>0.065590407</td></tr><tr><td></td><td></td><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td><td></td><td></td></tr></tbody></table>

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
| SAMD11       | 0           | -1          | 2           |
|              |             |             |             |
|              |             |             |             |



## Associated metadata files

For each type of data file, there needs to be an associated metadata file. A metadata file is a flat text file. If a meta file does not exist for the data file in your import file folder, the import will fail.

### How to prepare a metadata file?

For each type of data file, there are some optional fields to include. The following are the required fields for a metadata file for data files: mutation, fusion, CNA:

1. **cancer\_study**_**\_**_**identifier**: The same database _<mark style="color:red;">project name</mark>_ stated in the meta\_study.txt file
2. **genetic\_alteration**_**\_**_**type**: For each data file you are generating a meta file for, the value here will be different
   * mutation data file = MUTATION\_EXTENDED
   * fusion data file = FUSION
   * copy number alteration - discrete/continuous = COPY\_NUMBER\_ALTERATION
3. **data\_type**: The type of data this meta file is for. For each data file you are generating a meta file for, the value here will be different
   * mutation data file = MAF
   * fusion data file = FUSION
   * copy number alteration - discrete = DISCRETE
   * copy number alteration - continuous = CONTINUOUS or LOG2-VALUE
4. **stable\_id**: The data file type ID. For each data file you are generating a meta file for, the value here will be different
   * mutation data file = mutations
   * fusion data file = fusion
   * copy number alteration - discrete = gistic, cna, cna\_rae or cna\_consensus
   * copy number alteration - continuous = linear\_CNA or log2CNA
5. **profile\_name**: A name for the data. For each data file you are generating a meta file for, the value here will be different
   * mutation data file = e.g., "Mutations"
   * fusion data file = e.g., "Fusions"
   * copy number alteration - discrete = e.g., "Putative copy-number alterations from GISTIC"
   * copy number alteration - continuous = e.g., "copy-number values".
6. **profile\_description**: A short description of the data.&#x20;
7. **data\_filename**: The data file's filename is to be stated here
   * mutation data file = "data\_mutations\_extended.txt"
   * fusion data file = "data\_fusions.txt"
   * copy number alteration - discrete = "data\_cna.txt"
   * copy number alteration - continuous = "data\_log2\_cna.txt"

The metadata file's fields are slightly different for the segmented data's metadata file. The following are its required fields:

1. **cancer\_study**_**\_**_**identifier**: The same database _<mark style="color:red;">project name</mark>_ stated in the meta\_study.txt
2. **genetic\_alteration**_**\_**_**type**: COPY\_NUMBER\_ALTERATION
3. **data\_type**: SEG
4. **reference\_genome\_id**: The genome version of the data. Acceptable values: "hg19" or "hg38"
5. **description**: A short description of the segmented data
6. **data\_filename**: The data file's filename is to be stated here. e.g., "data\_segments.seg_"_

{% hint style="info" %}
Please note these are the common genomic data files. If there are other genomic data files to be included in the import, those data files also require its own metadata file as well. For more information on the [other genomic data](https://docs.cbioportal.org/file-formats/#expression-data) and how to prepare the data and the metadata file please refer to the official cBioPortal's documentation. (Hint: for ease of navigation their website has an organized navigation sidebar on the right of the webpage to help users)
{% endhint %}
