---
description: This is also known as the status timeline
---

# Timeline: Follow-up

## Timeline Follow-up Headers

All the MOHCCN field names under the _ICGC ARGO schema_ 'Follow Up'

<table><thead><tr><th width="158">PATIENT_ID</th><th width="141">START_DATE</th><th width="128">STOP_DATE</th><th width="143">EVENT_TYPE</th><th width="144">PROGRAM_ID</th><th width="264">SUBMITTER_FOLLOW_UP_ID</th><th width="331">SUBMITTER_PRIMARY_DIAGNOSIS_ID</th><th width="273">SUBMITTER_TREATMENT_ID</th><th width="212">DATE_OF_FOLLOWUP</th><th width="306">DISEASE_STATUS_AT_FOLLOWUP</th><th width="163">RELAPSE_TYPE</th><th width="191">DATE_OF_RELAPSE</th><th width="331">METHOD_OF_PROGRESSION_STATUS</th><th width="438">ANATOMIC_SITE_PROGRESSION_OR_RECURRENCE</th><th></th></tr></thead><tbody><tr><td>ABC-01-0001</td><td>199</td><td></td><td>Follow Up</td><td>ABC</td><td></td><td></td><td></td><td>2021-05</td><td>Stable</td><td>Local recurrence</td><td>2021-04</td><td>Assessment of symptom control (procedure)</td><td>Liver</td><td></td></tr><tr><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td></tr></tbody></table>

### Legend

Black and bold font are mandatory cBioportal headers.

#### No matter which type of timeline file you want to create, all timeline data files must contain these 4 columns in this order (left to right):

* **PATIENT\_ID** = "submitter\_donor\_id"
* **START\_DATE** = "interval\_of\_followup"
* **STOP\_DATE**: The end date of the event is calculated in days from the date of diagnosis (which will act as point zero on the timeline scale).
  * If the event occurs over time (e.g. a Treatment, ...) the STOP\_DATE column should have values.
  * If the event occurs at a time point (e.g. a Lab\_test, Imaging, ...) the STOP\_DATE is still mandatory, but the values should be blanks.
* **EVENT\_TYPE** = the category of the event; ie 'FOLLOW UP'

{% hint style="info" %}
For more information about the Timeline columns, please visit the [official cBioPortal Documentation](https://docs.cbioportal.org/5.1-data-loading/data-loading/file-formats#timeline-data), and our [Clinical Timeline Setup](../../file-formats/clinical-timeline-setup/) section
{% endhint %}
