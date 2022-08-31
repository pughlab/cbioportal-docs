# Sample File

## Sample Headers

All the MOHCCN field names under the _ICGC ARGO File_ of categories: 'Sample Registration', 'Specimen', and most of 'Primary Diagnosis' are located in this file as they pertain to the sample level attributes.

| **PATIENT\_ID** | **SAMPLE\_ID** | **CANCER\_TYPE** | **CANCER\_TYPE\_DETAILED** | **ONCOTREE\_CODE** | _<mark style="color:blue;">SAMPLE\_CLASS</mark>_ | PRIMARY\_SITE | SPECIMEN\_TISSUE\_SOURCE | TUMOUR\_NORMAL\_DESIGNATION | SPECIMEN\_TYPE | SUBMITTER\_SAMPLE\_ID | SAMPLE\_TYPE | SUBMITTER\_PRIMARY\_DIAGNOSIS\_ID | PATHOLOGICAL\_TUMOUR\_STAGING\_SYSTEM | PATHOLOGICAL\_T\_CATEGORY | PATHOLOGICAL\_N\_CATEGORY | PATHOLOGICAL\_M\_CATEGORY | PATHOLOGICAL\_STAGE\_GROUP | SPECIMEN\_ACQUISITION\_INTERVAL | TUMOUR\_HISTOLOGICAL\_TYPE | SPECIMEN\_ANATOMIC\_LOCATION | REFERENCE\_PATHOLOGY\_CONFIRMED | TUMOUR\_GRADING\_SYSTEM | TUMOUR\_GRADE | PERCENT\_TUMOUR\_CELLS | CANCER\_TYPE\_CODE | LYMPH\_NODES\_EXAMINED\_STATUS | NUMBER\_LYMPH\_NODES\_POSITIVE | CLINICAL\_TUMOUR\_STAGING\_SYSTEM | CLINICAL\_T\_CATEGORY | CLINICAL\_N\_CATEGORY | CLINICAL\_M\_CATEGORY | CLINICAL\_STAGE\_GROUP |
| --------------- | -------------- | ---------------- | -------------------------- | ------------------ | ------------------------------------------------ | ------------- | ------------------------ | --------------------------- | -------------- | --------------------- | ------------ | --------------------------------- | ------------------------------------- | ------------------------- | ------------------------- | ------------------------- | -------------------------- | ------------------------------- | -------------------------- | ---------------------------- | ------------------------------- | ----------------------- | ------------- | ---------------------- | ------------------ | ------------------------------ | ------------------------------ | --------------------------------- | --------------------- | --------------------- | --------------------- | ---------------------- |
|                 |                |                  |                            |                    |                                                  |               |                          |                             |                |                       |              |                                   |                                       |                           |                           |                           |                            |                                 |                            |                              |                                 |                         |               |                        |                    |                                |                                |                                   |                       |                       |                       |                        |
|                 |                |                  |                            |                    |                                                  |               |                          |                             |                |                       |              |                                   |                                       |                           |                           |                           |                            |                                 |                            |                              |                                 |                         |               |                        |                    |                                |                                |                                   |                       |                       |                       |                        |
|                 |                |                  |                            |                    |                                                  |               |                          |                             |                |                       |              |                                   |                                       |                           |                           |                           |                            |                                 |                            |                              |                                 |                         |               |                        |                    |                                |                                |                                   |                       |                       |                       |                        |

### Legend

Black and bold font are mandatory cBioportal headers

* **PATIENT\_ID** = "submitter\_donor\_id"
* **SAMPLE\_ID** = "submitter\_specimen\_id"
* The **CANCER\_TYPE** field would be the general cancer type name.\
  &#x20;       The name in the base level after ‘Tissue’ on the Oncotree Map\
  &#x20;               For example: “Lung”
* The **CANCER\_TYPE\_DETAILED** field would be the name of the specific cancer type (going down the Oncotree map)\
  &#x20;       For example: “Poorly Differentiated Non-Small Cell Lung Cancer”
* The **ONCOTREE\_CODE** field would be the acronym of the Cancer Type Detailed name in the “CANCER\_TYPE\_DETAILED” field\
  &#x20;       For example: “NSCLCPD”

![OncoTree Code Example](broken-reference)

#### cBioPortal suggested columns in _<mark style="color:blue;">blue italics</mark>_:

From the cBioPortal Documentation, the following columns affect the header of the patient view by adding text to the samples in the header:

* _<mark style="color:blue;">SAMPLE\_DISPLAY\_NAME</mark>_: displayed in addition to the ID
* _<mark style="color:blue;">SAMPLE\_CLASS</mark>_: classifies the sample and when this column is present, the samples on the patient view header becomes a different colour with an icon next to the SAMPLE\_ID
  * For example, values can be: cfDNA, Tumor, Primary, Metastasis, Xenograft, etc
* _<mark style="color:blue;">METASTATIC\_SITE</mark>_ or _<mark style="color:blue;">PRIMARY\_SITE</mark>_: Override _<mark style="color:blue;">TUMOR\_SITE</mark>_ (patient level attribute) depending on sample type

The following columns additionally affect the Timeline data visualization:

* _<mark style="color:blue;">SAMPLE\_TYPE</mark>_, _<mark style="color:blue;">TUMOR\_TISSUE\_SITE</mark>_ or _<mark style="color:blue;">TUMOR\_TYPE</mark>_: gives sample icon in the timeline a colour.
  * If set to recurrence, recurred, progression or progressed: orange
  * If set to metastatic or metastasis: red
  * If set to primary or otherwise: black

{% hint style="info" %}
For more information about the clinical sample columns, please visit the [official cBioPortal documentation](https://docs.cbioportal.org/5.1-data-loading/data-loading/file-formats#clinical-sample-columns), and our [MetaData Standardization](../../file-formats/clinical-files-format/metadata-standardization.md) and [Clinical Sample File: OncoTree Code](../../file-formats/clinical-files-format/clinical-sample-file-oncotree-code.md) pages within the File Formats section
{% endhint %}
