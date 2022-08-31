# Timeline: Treatment Radiation Therapy

## Timeline Treatment Radiation Therapy Headers

All the MOHCCN field names under the _ICGC ARGO File_ of category 'Radiation'

| **PATIENT\_ID** | **START\_DATE** | **STOP\_DATE** | **EVENT\_TYPE** | _<mark style="color:blue;">TREATMENT\_TYPE</mark>_ | _<mark style="color:blue;">SUBTYPE</mark>_ | SUBMITTER\_TREATMENT\_ID | RADIATION\_THERAPY\_MODALITY | RADIATION\_THERAPY\_TYPE | RADIATION\_THERAPY\_FRACTIONS | RADIATION\_THERAPY\_DOSAGE | ANATOMICAL\_SITE\_IRRADIATED |
| --------------- | --------------- | -------------- | --------------- | -------------------------------------------------- | ------------------------------------------ | ------------------------ | ---------------------------- | ------------------------ | ----------------------------- | -------------------------- | ---------------------------- |
|                 |                 |                | TREATMENT       | Radiation Therapy                                  |                                            |                          |                              |                          |                               |                            |                              |
|                 |                 |                | TREATMENT       | Radiation Therapy                                  |                                            |                          |                              |                          |                               |                            |                              |

### Legend

Black and bold font are mandatory cBioportal headers

* **PATIENT\_ID** = "submitter\_donor\_id"
* **START\_DATE**: the start point of any event, calculated in \*days from the date of diagnosis (which will act as point zero on the timeline scale)
* **STOP\_DATE**: The end date of the event is calculated in days from the date of diagnosis (which will act as point zero on the timeline scale).
  * If the event occurs over time (e.g. a Treatment, ...) the STOP\_DATE column should have values.
  * If the event occurs at a time point (e.g. a Lab\_test, Imaging, ...) the STOP\_DATE is still mandatory, but the values should be blanks.
* **EVENT\_TYPE** = 'TREATMENT'
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
