# Timeline: Treatment Medical Therapy

## Timeline: Treatment Medical Therapy Headers

All the MOHCCN field names under the _ICGC ARGO schema_ 'Treatment' and 'Systemic Therapy' are included in the cBioportal Timeline Treatment Medical Therapy File. Their 'treatment\_type' and 'systemic\_therapy\_type' fields' permissible values fall under SUBTYPE in cBioPortal data categorization.

<table><thead><tr><th width="147">PATIENT_ID</th><th width="146">START_DATE</th><th width="134">STOP_DATE</th><th width="145">EVENT_TYPE</th><th width="196">TREATMENT_TYPE</th><th width="123">SUBTYPE</th><th width="164">AGENT</th><th width="151">AGENT_CLASS</th><th width="151">PROGRAM_ID</th><th width="270">SUBMITTER_TREATMENT_ID</th><th width="331">SUBMITTER_PRIMARY_DIAGNOSIS_ID</th><th width="247">IS_PRIMARY_TREATMENT</th><th width="205">TREATMENT_INTENT</th><th width="430">RESPONSE_TO_TREATMENT_CRITERIA_METHOD</th><th width="267">RESPONSE_TO_TREATMENT</th><th width="241">STATUS_OF_TREATMENT</th><th width="184">DAYS_PER_CYCLE</th><th width="209">NUMBER_OF_CYCLES</th><th width="284">DRUG_REFERENCE_DATABASE</th><th width="280">DRUG_REFERENCE_IDENTIFIER</th><th width="189">DRUG_DOSE_UNITS</th><th width="360">PRESCRIBED_CUMULATIVE_DRUG_DOSE</th><th width="322">ACTUAL_CUMULATIVE_DRUG_DOSE</th><th></th></tr></thead><tbody><tr><td>ABC-02-0005</td><td>0</td><td>8</td><td>TREATMENT</td><td>Medical Therapy</td><td><mark style="background-color:orange;">Chemotherapy</mark></td><td>Bortezomib</td><td>PI</td><td>ABC</td><td></td><td></td><td>Yes</td><td>Curative</td><td></td><td></td><td>Physician decision (stopped or interrupted treatment)</td><td>1</td><td>2</td><td>Rxnorm</td><td>402244</td><td>mg/m2</td><td>8</td><td>8</td><td></td></tr><tr><td>ABC-02-0005</td><td>15</td><td>37</td><td>TREATMENT</td><td>Medical Therapy</td><td><mark style="background-color:orange;">Chemotherapy</mark></td><td>Ixazomib</td><td>PI</td><td>ABC</td><td></td><td></td><td>No</td><td>Supportive</td><td></td><td></td><td>Treatment stopped due to lack of efficacy (disease progression)</td><td>3</td><td>3</td><td>Rxnorm</td><td>1723763</td><td>mg/m2</td><td>1.5</td><td>1.5</td><td></td></tr><tr><td>ABC-01-0101</td><td>1</td><td>52</td><td>TREATMENT</td><td>Medical Therapy</td><td><mark style="background-color:blue;">Hormone Therapy</mark></td><td>Goserelin</td><td></td><td>ABC</td><td></td><td></td><td>Yes</td><td>Palliative</td><td></td><td></td><td>Treatment incomplete due to technical or organizational problems</td><td>2</td><td>1</td><td>PubChem</td><td>5311128</td><td>mg/m2</td><td>3.5</td><td>3.5</td><td></td></tr><tr><td>ABC-03-0987</td><td>20</td><td>63</td><td>TREATMENT</td><td>Medical Therapy</td><td><mark style="background-color:red;">Immunotherapy</mark></td><td>Pembrolizumab</td><td></td><td>ABC</td><td></td><td></td><td>Yes</td><td>Curative</td><td></td><td></td><td>Treatment completed as prescribed</td><td>3</td><td>4</td><td>NCI Thesaurus</td><td>C106432</td><td>mg/m2</td><td></td><td></td><td></td></tr></tbody></table>

### Legend

Black and bold font are mandatory cBioportal headers

* **PATIENT\_ID** = "submitter\_donor\_id"
* **START\_DATE**: the start point of any event, calculated in \*days from the date of diagnosis (which will act as point zero on the timeline scale) <- "TREATMENT\_START\_DATE"
* **STOP\_DATE**: The end date of the event is calculated in days from the date of diagnosis (which will act as point zero on the timeline scale) <- "TREATMENT\_STOP\_DATE"
* **EVENT\_TYPE** = 'TREATMENT'
* _<mark style="color:blue;">SUBTYPE</mark>_ = ARGO's "treatment\_type" values
* _<mark style="color:blue;">AGENT</mark>_ = "drug\_name"

#### cBioPortal suggested columns in _<mark style="color:blue;">blue italics:</mark>_

* _<mark style="color:blue;">TREATMENT\_TYPE</mark>_: This can be either Medical Therapy or Radiation Therapy.
* _<mark style="color:blue;">SUBTYPE</mark>_: Depending upon the TREATMENT\_TYPE, this can either be Chemotherapy, Hormone Therapy, Targeted Therapy etc. (for Medical Therapies) or WPRT, IVRT etc. (for Radiation Therapies).
* _<mark style="color:blue;">AGENT</mark>_: for medical therapies, the agent is defined with number of cycles if applicable and for radiation therapy, the agent is defined as standard dose given to the patient during the course.
* _<mark style="color:blue;">AGENT\_CLASS</mark>_: This allows you to classify your agents into useful groups.
* <mark style="color:red;">Special</mark>: When using the _<mark style="color:blue;">AGENT</mark>_ and _<mark style="color:blue;">SUBTYPE</mark>_ columns, each agent and subtype will be split into its own track.

{% hint style="info" %}
For more information about the Timeline columns, please visit the [official cBioPortal Documentation](https://docs.cbioportal.org/5.1-data-loading/data-loading/file-formats#timeline-data), and our [Clinical Timeline Setup](../../file-formats/clinical-timeline-setup/) section
{% endhint %}

