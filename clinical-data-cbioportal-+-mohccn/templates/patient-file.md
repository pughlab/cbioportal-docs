# Patient File

## Patient Headers

The MOHCCN field names under the ICGC ARGO schemas 'Donor', 'Primary Diagnosis', 'Comorbidity', and 'Exposure' are located in this file as they pertain to the patient level attributes

<table><thead><tr><th width="143">PATIENT_ID</th><th width="108">GENDER</th><th width="87">AGE</th><th width="124">OS_STATUS</th><th width="144">OS_MONTHS</th><th width="136">DFS_STATUS</th><th width="143">DFS_MONTHS</th><th width="143">TUMOR_SITE</th><th width="87">SEX</th><th width="145">IS_DECEASED</th><th width="171">DATE_OF_BIRTH</th><th width="174">DATE_OF_DEATH</th><th width="191">DATE_RESOLUTION</th><th width="177">CAUSE_OF_DEATH</th><th width="513">LOST_TO_FOLLOWUP_AFTER_CLINICAL_EVENT_IDENTIFIER</th><th width="291">LOST_TO_FOLLOWUP_REASON</th><th width="377">DATE_ALIVE_AFTER_LOST_TO_FOLLOWUP</th><th width="332">SUBMITTER_PRIMARY_DIAGNOSIS_ID</th><th width="208">DATE_OF_DIAGNOSIS</th><th width="208">CANCER_TYPE_CODE</th><th width="210">BASIS_OF_DIAGNOSIS</th><th width="138">LATERALITY</th><th width="344">CLINICAL_TUMOUR_STAGING_SYSTEM</th><th width="222">CLINICAL_T_CATEGORY</th><th width="229">CLINICAL_N_CATEGORY</th><th width="231">CLINICAL_M_CATEGORY</th><th width="236">CLINICAL_STAGE_GROUP</th><th width="392">PATHOLOGICAL_TUMOUR_STAGING_SYSTEM</th><th width="275">PATHOLOGICAL_T_CATEGORY</th><th width="274">PATHOLOGICAL_N_CATEGORY</th><th width="273">PATHOLOGICAL_M_CATEGORY</th><th width="282">PATHOLOGICAL_STAGE_GROUP</th><th width="204">PRIOR_MALIGNANCY</th><th width="341">LATERALITY_OF_PRIOR_MALIGNANCY</th><th width="318">AGE_AT_COMORBIDITY_DIAGNOSIS</th><th width="257">COMORBIDITY_TYPE_CODE</th><th width="333">COMORBIDITY_TREATMENT_STATUS</th><th width="259">COMORBIDITY_TREATMENT</th><th width="277">TOBACCO_SMOKING_STATUS</th><th width="133">TOBACCO_TYPE</th><th width="222">PACK_YEARS_SMOKED</th><th></th></tr></thead><tbody><tr><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td></tr></tbody></table>

### Legend

Black and bold font are mandatory cBioportal headers

* **PATIENT\_ID** = "submitter\_donor\_id"
* _<mark style="color:blue;">AGE</mark>_ = "age\_of\_diagnosis"

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
