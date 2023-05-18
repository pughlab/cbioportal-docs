# Patient File

## Patient Headers

The MOHCCN field names under the ICGC ARGO File schemas: 'Donor', 'Primary Diagnosis', 'Comorbidity', and 'Exposure' are located in this file as they pertain to the patient level attributes

| PATIENT\_ID | GENDER | AGE | OS\_STATUS | OS\_MONTHS | DFS\_STATUS | DFS\_MONTHS | TUMOR\_SITE | SEX\_AT\_BIRTH | IS\_DECEASED | CAUSE\_OF\_DEATH | DATE\_OF\_BIRTH | DATE\_OF\_DEATH | LOST\_TO\_FOLLOWUP\_AFTER\_CLINICAL\_EVENT\_IDENTIFIER | LOST\_TO\_FOLLOWUP\_REASON | DATE\_ALIVE\_AFTER\_LOST\_TO\_FOLLOWUP | DATE\_OF\_DIAGNOSIS | BASIS\_OF\_DIAGNOSIS | CANCER\_TYPE\_CODE | LATERALITY | LYMPH\_NODES\_EXAMINED\_STATUS | LYMPH\_NODES\_EXAMINED\_METHOD | NUMBER\_LYMPH\_NODES\_POSITIVE | CLINICAL\_TUMOUR\_STAGING\_SYSTEM | CLINICAL\_T\_CATEGORY | CLINICAL\_N\_CATEGORY | CLINICAL\_M\_CATEGORY | CLINICAL\_STAGE\_GROUP | PRIOR\_MALIGNANCY | LATERALITY\_OF\_PRIOR\_MALIGNANCY | AGE\_AT\_COMORBIDITY\_DIAGNOSIS | COMORBIDITY\_TYPE\_CODE | COMORBIDITY\_TREATMENT\_STATUS | COMORBIDITY\_TREATMENT | TOBACCO\_SMOKING\_STATUS | TOBACCO\_TYPE | PACK\_YEARS\_SMOKED |
| ----------- | ------ | --- | ---------- | ---------- | ----------- | ----------- | ----------- | -------------- | ------------ | ---------------- | --------------- | --------------- | ------------------------------------------------------ | -------------------------- | -------------------------------------- | ------------------- | -------------------- | ------------------ | ---------- | ------------------------------ | ------------------------------ | ------------------------------ | --------------------------------- | --------------------- | --------------------- | --------------------- | ---------------------- | ----------------- | --------------------------------- | ------------------------------- | ----------------------- | ------------------------------ | ---------------------- | ------------------------ | ------------- | ------------------- |
|             |        |     |            |            |             |             |             |                |              |                  |                 |                 |                                                        |                            |                                        |                     |                      |                    |            |                                |                                |                                |                                   |                       |                       |                       |                        |                   |                                   |                                 |                         |                                |                        |                          |               |                     |
|             |        |     |            |            |             |             |             |                |              |                  |                 |                 |                                                        |                            |                                        |                     |                      |                    |            |                                |                                |                                |                                   |                       |                       |                       |                        |                   |                                   |                                 |                         |                                |                        |                          |               |                     |
|             |        |     |            |            |             |             |             |                |              |                  |                 |                 |                                                        |                            |                                        |                     |                      |                    |            |                                |                                |                                |                                   |                       |                       |                       |                        |                   |                                   |                                 |                         |                                |                        |                          |               |                     |

### Legend

Black and bold font are mandatory cBioportal headers

* **PATIENT\_ID** = "submitter\_donor\_id"
* _<mark style="color:blue;">AGE</mark>_ = "age\_of\_diagnosis"
* SURVIVAL\_TIME: According to the MOHCCN fields, this is field is in DAYS
  * whereas cBioPortal’s field for this is ‘OS\_MONTHS’ == Overall Survival Months

#### &#x20;cBioPortal suggested columns are in _<mark style="color:blue;">blue italics</mark>_:

* _<mark style="color:blue;">OS\_STATUS</mark>_: Overall patient survival status. \
  &#x20;Possible values: 1:DECEASED, 0:LIVING\
  &#x20;In the patient view, 0:LIVING creates a green label, 1:DECEASED a red label.&#x20;
* _<mark style="color:blue;">OS\_MONTHS</mark>_: Overall survival in months since initial diagnosis&#x20;
* _<mark style="color:blue;">DFS\_STATUS</mark>_: Disease free status since initial treatment\
  &#x20;Possible values: 0:DiseaseFree, 1:Recurred/Progressed\
  &#x20;In the patient view, 0:DiseaseFree creates a green label, 1:Recurred/Progressed a red label.&#x20;
* _<mark style="color:blue;">DFS\_MONTHS</mark>_: Disease free (months) since initial treatment

These columns, when provided, add additional information to the patient description in the header:

* _<mark style="color:blue;">GENDER</mark>_ or _<mark style="color:blue;">SEX</mark>_: Gender or sex of the patient (string)
* _<mark style="color:blue;">AGE</mark>_: Age at which the condition or disease was first diagnosed, in years (number)
* _<mark style="color:blue;">TUMOR\_SITE</mark>_

{% hint style="info" %}
For more information about cBioPortal clinical patient columns please visit the [official cBioportal Documentation](https://docs.cbioportal.org/5.1-data-loading/data-loading/file-formats#clinical-patient-columns) and our [MetaData Standardization](../../file-formats/clinical-files-format/metadata-standardization.md) section
{% endhint %}
