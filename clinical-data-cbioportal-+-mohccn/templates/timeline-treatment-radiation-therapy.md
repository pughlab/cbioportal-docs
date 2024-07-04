# Timeline: Treatment Radiation Therapy

## Timeline Treatment Radiation Therapy Headers

All the MOHCCN field names under the _ICGC ARGO schema_ 'Radiation'

<table data-header-hidden><thead><tr><th width="171"></th><th width="157"></th><th width="140"></th><th width="144"></th><th width="194"></th><th width="200"></th><th width="156"></th><th width="264"></th><th width="303"></th><th width="257"></th><th width="306"></th><th width="281"></th><th width="294"></th><th width="186"></th><th width="368"></th><th></th></tr></thead><tbody><tr><td><strong>PATIENT_ID</strong></td><td><strong>START_DATE</strong></td><td><strong>STOP_DATE</strong></td><td><strong>EVENT_TYPE</strong></td><td><em><mark style="color:blue;">TREATMENT_TYPE</mark></em></td><td><em><mark style="color:blue;">SUBTYPE</mark></em></td><td>PROGRAM_ID</td><td>SUBMITTER_TREATMENT_ID</td><td>RADIATION_THERAPY_MODALITY</td><td>RADIATION_THERAPY_TYPE</td><td>RADIATION_THERAPY_FRACTIONS</td><td>RADIATION_THERAPY_DOSAGE</td><td>ANATOMICAL_SITE_IRRADIATED</td><td>RADIATION_BOOST</td><td>REFERENCE_RADIATION_TREATMENT_ID</td><td></td></tr><tr><td>ABC-01-0001</td><td>80</td><td></td><td>TREATMENT</td><td>Radiation Therapy</td><td></td><td>ABC</td><td></td><td>Brachytherapy (procedure)</td><td>External</td><td>20</td><td>5</td><td>Chest wall structure (body structure)</td><td>No</td><td></td><td></td></tr></tbody></table>

### Legend

Black and bold font are mandatory cBioportal headers

* **PATIENT\_ID** = "submitter\_donor\_id"
* **START\_DATE**: "TREATMENT\_START\_DATE"
* **STOP\_DATE**: "TREATMENT\_STOP\_DATE"
* **EVENT\_TYPE** = 'TREATMENT'
* _<mark style="color:blue;">TREATMENT\_TYPE</mark>_: Radiation Therapy
* _<mark style="color:blue;">SUBTYPE</mark>_ = ARGO's "treatment\_type" values

#### cBioPortal suggested columns in _<mark style="color:blue;">blue italics</mark>_:

* _<mark style="color:blue;">TREATMENT\_TYPE</mark>_: This can be either Medical Therapy or Radiation Therapy.
* _<mark style="color:blue;">SUBTYPE</mark>_: Depending upon the TREATMENT\_TYPE, this can either be Chemotherapy, Hormone Therapy, Targeted Therapy etc. (for Medical Therapies) or WPRT, IVRT etc. (for Radiation Therapies).
* _<mark style="color:blue;">AGENT</mark>_: for medical therapies, the agent is defined with number of cycles if applicable and for radiation therapy, the agent is defined as standard dose given to the patient during the course.
* _<mark style="color:blue;">AGENT\_CLASS</mark>_: This allows you to classify your agents into useful groups.
* <mark style="color:red;">Special</mark>: When using the _<mark style="color:blue;">AGENT</mark>_ and _<mark style="color:blue;">SUBTYPE</mark>_ columns, each agent and subtype will be split into its own track.

{% hint style="info" %}
For more information about the Timeline columns, please visit the [official cBioPortal Documentation](https://docs.cbioportal.org/5.1-data-loading/data-loading/file-formats#timeline-data), and our [Clinical Timeline Setup](../../file-formats/clinical-timeline-setup/) section
{% endhint %}
