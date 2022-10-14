---
description: >-
  Details of the Various Treatments mentioned in the Timeline Treatment file
  (previous page)
---

# Timeline: Treatment

## Timeline: Treatment Medical Therapy Headers

All the MOHCCN field names under the _ICGC ARGO File_ of categories: 'Chemotherapy', 'Hormone Therapy',  'Immunotherapy' which all are subtypes that fall under TREATMENT\_TYPE "Medical Therapy" in cBioPortal

| **PATIENT\_ID** | **START\_DATE** | **STOP\_DATE** | **EVENT\_TYPE** | _<mark style="color:blue;">TREATMENT\_TYPE</mark>_ | _<mark style="color:blue;">SUBTYPE</mark>_                  | _<mark style="color:blue;">AGENT</mark>_ | _<mark style="color:blue;">AGENT\_CLASS</mark>_ | PROGRAM\_ID | SUBMITTER\_TREATMENT\_ID | SUBMITTER\_PRIMARY\_DIAGNOSIS\_ID | DRUG\_RXNORMCUI | DOSAGE\_UNITS | CUMULATIVE\_DRUG\_DOSAGE\_PRESCRIBED | CUMULATIVE\_DRUG\_DOSAGE\_ACTUAL | <mark style="background-color:red;">IMMUNOTHERAPY\_TYPE</mark> | IS\_PRIMARY\_TREATMENT | TREATMENT\_SETTING  | TREATMENT\_INTENT | DAYS\_PER\_CYCLE | NUMBER\_OF\_CYCLES | RESPONSE\_TO\_TREATMENT\_CRITERIA\_METHOD | RESPONSE\_TO\_TREATMENT |
| --------------- | --------------- | -------------- | --------------- | -------------------------------------------------- | ----------------------------------------------------------- | ---------------------------------------- | ----------------------------------------------- | ----------- | ------------------------ | --------------------------------- | --------------- | ------------- | ------------------------------------ | -------------------------------- | -------------------------------------------------------------- | ---------------------- | ------------------- | ----------------- | ---------------- | ------------------ | ----------------------------------------- | ----------------------- |
| ABC-02-0005     | 0               | 8              | TREATMENT       | Medical Therapy                                    | <mark style="background-color:orange;">Chemotherapy</mark>  | Bortezomib                               | PI                                              |             |                          |                                   | Bortezomib      | mg/m2         | 8                                    | 8                                |                                                                | Yes                    | Adjuvant            | Curative          | 5                | 1                  |                                           |                         |
| ABC-02-0005     | 15              | 37             | TREATMENT       | Medical Therapy                                    | <mark style="background-color:orange;">Chemotherapy</mark>  | Ixazomib                                 | PI                                              |             |                          |                                   | Ixazomib        | mg/m2         | 1.5                                  | 1.5                              |                                                                | Yes                    | Advanced/Metastatic | Curative          | 12               | 1                  |                                           |                         |
| ABC-01-0101     | 1               | 52             | TREATMENT       | Medical Therapy                                    | <mark style="background-color:blue;">Hormone Therapy</mark> | Goserelin                                |                                                 |             |                          |                                   | Goserelin       | mg/m2         | 3.5                                  | 3.5                              |                                                                | Unknown                | Advanced/Metastatic | Curative          | 8                | 3                  |                                           |                         |
| ABC-03-0987     | 20              | 63             | TREATMENT       | Medical Therapy                                    | <mark style="background-color:red;">Immunotherapy</mark>    | Pembrolizumab                            |                                                 |             |                          |                                   | Pembrolizumab   |               |                                      |                                  |                                                                | No                     | Advanced/Metastatic | Palliative        | 15               | 2                  |                                           |                         |

### Legend

Black and bold font are mandatory cBioportal headers

* **PATIENT\_ID** = "submitter\_donor\_id"
* **START\_DATE**: the start point of any event, calculated in \*days from the date of diagnosis (which will act as point zero on the timeline scale) <- "TREATMENT\_START\_DATE"
* **STOP\_DATE**: The end date of the event is calculated in days from the date of diagnosis (which will act as point zero on the timeline scale) <- "TREATMENT\_STOP\_DATE"
* **EVENT\_TYPE** = 'TREATMENT'
* _<mark style="color:blue;">SUBTYPE</mark>_ = ARGO's "treatment\_type" values
* _<mark style="color:blue;">AGENT</mark>_ = "drug\_name"

"chemotherapy\_dosage\_units" = "hormone\_drug\_dosage\_units" <- therefore, will be DOSAGE\_UNITS

"cumulative\_drug\_dosage\_prescribed" & "cumulative\_drug\_dosage\_actual"<- same columns occurs for both Chemotherapy and Hormone Therapy schema profiles

#### cBioPortal suggested columns in _<mark style="color:blue;">blue italics:</mark>_

* _<mark style="color:blue;">TREATMENT\_TYPE</mark>_: This can be either Medical Therapy or Radiation Therapy.
* _<mark style="color:blue;">SUBTYPE</mark>_: Depending upon the TREATMENT\_TYPE, this can either be Chemotherapy, Hormone Therapy, Targeted Therapy etc. (for Medical Therapies) or WPRT, IVRT etc. (for Radiation Therapies).
* _<mark style="color:blue;">AGENT</mark>_: for medical therapies, the agent is defined with number of cycles if applicable and for radiation therapy, the agent is defined as standard dose given to the patient during the course.
* _<mark style="color:blue;">AGENT\_CLASS</mark>_: This allows you to classify your agents into useful groups.
* <mark style="color:red;">Special</mark>: When using the _<mark style="color:blue;">AGENT</mark>_ and _<mark style="color:blue;">SUBTYPE</mark>_ columns, each agent and subtype will be split into its own track.

{% hint style="info" %}
For more information about the Timeline columns, please visit the [official cBioPortal Documentation](https://docs.cbioportal.org/5.1-data-loading/data-loading/file-formats#timeline-data), and our [Clinical Timeline Setup](../../file-formats/clinical-timeline-setup/) section
{% endhint %}

