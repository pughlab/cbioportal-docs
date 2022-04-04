# Patient File

## Patient Headers

The MOHCCN field names under the _ICGC ARGO File_ categories 'Donor' and a few from 'Primary Diagnosis' are located in this file as they pertain to the patient level attributes

| **PATIENT\_ID** | <mark style="color:blue;">GENDER</mark> | _<mark style="color:blue;">AGE</mark>_ | VITAL\_STATUS | CAUSE\_OF\_DEATH | SURVIVAL\_TIME | _<mark style="color:blue;">OS\_STATUS</mark>_ | _<mark style="color:blue;">OS\_MONTHS</mark>_ | _<mark style="color:blue;">DFS\_STATUS</mark>_ | _<mark style="color:blue;">DFS\_MONTHS</mark>_ | _<mark style="color:blue;">TUMOR\_SITE</mark>_ |
| --------------- | --------------------------------------- | -------------------------------------- | ------------- | ---------------- | -------------- | --------------------------------------------- | --------------------------------------------- | ---------------------------------------------- | ---------------------------------------------- | ---------------------------------------------- |
|                 |                                         |                                        |               |                  |                |                                               |                                               |                                                |                                                |                                                |
|                 |                                         |                                        |               |                  |                |                                               |                                               |                                                |                                                |                                                |

### Legend

Black and bold font are mandatory cBioportal headers

* **PATIENT\_ID** = "submitter\_donor\_id"
* <mark style="color:blue;">AGE</mark> = "age\_of\_diagnosis"
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

* _<mark style="color:blue;">GENDER</mark> _ or _<mark style="color:blue;">SEX</mark>_: Gender or sex of the patient (string)
* _<mark style="color:blue;">AGE</mark>_: Age at which the condition or disease was first diagnosed, in years (number)
* _<mark style="color:blue;">TUMOR\_SITE</mark>_

{% hint style="info" %}
For more information about cBioPortal clinical patient columns please visit the [official cBioportal Documentation](https://docs.cbioportal.org/5.1-data-loading/data-loading/file-formats#clinical-patient-columns) and our [MetaData Standardization](../../file-formats/clinical-files-format/metadata-standardization.md) section
{% endhint %}

### \*Patient file template download\*

{% hint style="warning" %}
The template is in excel for the user's ease in filling out the data. However, for the actual cBioPortal project import, the file is to be in tab-delimited format. Please do not include empty columns or extra spaces, as these will give errors upon import.
{% endhint %}
