# Timeline: Treatment Radiation Therapy

## Timeline Treatment Radiation Therapy Headers

All the MOHCCN field names under the _ICGC ARGO File_ of category 'Radiation'

| **PATIENT\_ID** | **START\_DATE** | **STOP\_DATE** | **EVENT\_TYPE** | _<mark style="color:blue;">TREATMENT\_TYPE</mark>_ | _<mark style="color:blue;">SUBTYPE</mark>_ | PROGRAM\_ID | SUBMITTER\_TREATMENT\_ID | RADIATION\_THERAPY\_MODALITY | RADIATION\_THERAPY\_TYPE | RADIATION\_THERAPY\_FRACTIONS | RADIATION\_THERAPY\_DOSAGE | ANATOMICAL\_SITE\_IRRADIATED          | RADIATION\_BOOST | REFERENCE\_RADIATION\_TREATMENT\_ID |
| --------------- | --------------- | -------------- | --------------- | -------------------------------------------------- | ------------------------------------------ | ----------- | ------------------------ | ---------------------------- | ------------------------ | ----------------------------- | -------------------------- | ------------------------------------- | ---------------- | ----------------------------------- |
| ABC-01-0001     | 80              |                | TREATMENT       | Radiation Therapy                                  |                                            |             |                          | Brachytherapy (procedure)    | External                 | 20                            | 5                          | Chest wall structure (body structure) |                  |                                     |

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
