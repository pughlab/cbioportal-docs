# Timeline: Relapse

## Timeline Relapse Headers

All the MOHCCN field names under the ICGC ARGO schema 'Follow Up' -  the relapse fields. Since we have the "date\_of\_relapse" data available, we can create another timeline, if the user wishes

| PATIENT\_ID | START\_DATE | STOP\_DATE | EVENT\_TYPE | PROGRAM\_ID | RELAPSE\_TYPE | DATE\_OF\_RELAPSE | METHOD\_OF\_PROGRESSION\_STATUS | ANATOMIC\_SITE\_PROGRESSION\_OR\_RECURRENCE |
| ----------- | ----------- | ---------- | ----------- | ----------- | ------------- | ----------------- | ------------------------------- | ------------------------------------------- |
|             |             |            | RELAPSE     |             |               |                   |                                 |                                             |
|             |             |            |             |             |               |                   |                                 |                                             |

### Legend

Black and bold font are mandatory cBioportal headers

* **PATIENT\_ID** = "submitter\_donor\_id"
* **START\_DATE** = "DATE\_OF\_RELAPSE" - "date\_of\_diagnosis" = days (integer value)
* **STOP\_DATE**: BLANK
* **EVENT\_TYPE** = RELAPSE
