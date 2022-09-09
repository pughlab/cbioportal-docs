# Timeline: Specimen

## Timeline: Specimen Headers

As the timeline specimen file is closely aligned with the sample file, all those fields regarding sample attributes are in the clinical samples file, to have concise data and to avoid data duplication. The "specimen\_acquisition\_interval" field name from the MOHCCN fields is relevant for a specimen timeline

| **PATIENT\_ID** | **START\_DATE** | **STOP\_DATE** | **EVENT\_TYPE** | **SAMPLE\_ID**     |
| --------------- | --------------- | -------------- | --------------- | ------------------ |
| ABC-01-0023     | 15              |                | SPECIMEN        | ABC-01-0023-alpha1 |
| ABC-01-0023     | 2551            |                | SPECIMEN        | ABC-01-0023-alpha2 |
| ABC-02-0008     | 6               |                | SPECIMEN        | ABC-02-0008-alpha1 |

### Legend

Black and bold font are mandatory cBioportal headers

* **PATIENT\_ID** = "submitter\_donor\_id"
* **START\_DATE** = "specimen\_acquisition\_interval"
* **STOP\_DATE** = _BLANK_
* **EVENT\_TYPE** = 'SPECIMEN'
* **SAMPLE\_ID** = "submitter\_specimen\_id"

No matter which type of timeline file you want to create, all timeline data files MUST contain these 4 columns in this order (left to right):

1. **PATIENT\_ID**: the patient ID from the dataset
2. **START\_DATE**: the start point of a specimen event, a singular time point. The date of sample collection is required, subtracted by the date of diagnosis (which will act as point zero on the timeline scale), giving you an integer value
3. **STOP\_DATE**: Leave the STOP\_DATE blank
4. **EVENT\_TYPE**: the category of the event is _SPECIMEN_ here

{% hint style="info" %}
For more information about the Timeline columns, please visit the [official cBioPortal Documentation](https://docs.cbioportal.org/5.1-data-loading/data-loading/file-formats#timeline-data), and our [Clinical Timeline Setup](../../file-formats/clinical-timeline-setup/) section
{% endhint %}

{% hint style="warning" %}
**Attention**: Some clinical attributes affect the timeline visualization. Please check the [Clinical Data](https://docs.cbioportal.org/5.1-data-loading/data-loading/file-formats#clinical-data) section for more information.
{% endhint %}
