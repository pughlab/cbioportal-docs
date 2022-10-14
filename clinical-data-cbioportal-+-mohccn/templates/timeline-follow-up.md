---
description: This is also known as the status timeline
---

# Timeline: Follow-up

## Timeline Follow-up Headers

All the MOHCCN field names under the _ICGC ARGO File_ of category 'Follow Up'

| **PATIENT\_ID** | **START\_DATE** | **STOP\_DATE** | **EVENT\_TYPE** | PROGRAM\_ID | SUBMITTER\_FOLLOW\_UP\_ID | SUBMITTER\_PRIMARY\_DIAGNOSIS\_ID | SUBMITTER\_TREATMENT\_ID | DATE\_OF\_FOLLOWUP | LOST\_TO\_FOLLOWUP | LOST\_TO\_FOLLOWUP\_REASON | DISEASE\_STATUS\_AT\_FOLLOWUP | RELAPSE\_TYPE    | DATE\_OF\_RELAPSE | METHOD\_OF\_PROGRESSION\_STATUS           | ANATOMIC\_SITE\_PROGRESSION\_OR\_RECURRENCE | RECURRENCE\_TUMOUR\_STAGING\_SYSTEM | RECURRENCE\_T\_CATEGORY | RECURRENCE\_N\_CATEGORY | RECURRENCE\_M\_CATEGORY | RECURRENCE\_STAGE\_GROUP |
| --------------- | --------------- | -------------- | --------------- | ----------- | ------------------------- | --------------------------------- | ------------------------ | ------------------ | ------------------ | -------------------------- | ----------------------------- | ---------------- | ----------------- | ----------------------------------------- | ------------------------------------------- | ----------------------------------- | ----------------------- | ----------------------- | ----------------------- | ------------------------ |
| ABC-01-0001     | 199             |                | FOLLOW UP       |             |                           |                                   |                          |                    |                    |                            | Stable                        | Local recurrence |                   | Assessment of symptom control (procedure) |                                             |                                     |                         |                         |                         |                          |
|                 |                 |                | FOLLOW UP       |             |                           |                                   |                          |                    |                    |                            |                               |                  |                   |                                           |                                             |                                     |                         |                         |                         |                          |

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
