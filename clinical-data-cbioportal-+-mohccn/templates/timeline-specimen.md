# Timeline: Specimen

## Timeline: Specimen Headers

As the timeline specimen file is closely aligned with the sample file, all those fields regarding sample attributes are in the clinical samples file, to have concise data and to avoid data duplication. The "specimen\_acquisition\_interval" field name from the MOHCCN fields is relevant for a specimen timeline

| **PATIENT\_ID** | **START\_DATE** | **STOP\_DATE** | **EVENT\_TYPE** | **SAMPLE\_ID** |
| --------------- | --------------- | -------------- | --------------- | -------------- |
|                 |                 |                | SPECIMEN        |                |
|                 |                 |                | SPECIMEN        |                |

### Legend

Black and bold font are mandatory cBioportal headers

* **PATIENT\_ID** = "submitter\_donor\_id"
* **START\_DATE** = "specimen\_acquisition\_interval"
* **STOP\_DATE** = BLANK
* **EVENT\_TYPE** = the category of the event
* **SAMPLE\_ID** = "submitter\_specimen\_id"

No matter which type of timeline file you want to create, all timeline data files MUST contain these 4 columns in this order (left to right):

1. **PATIENT\_ID**: the patient ID from the dataset
2. **START\_DATE**: the start point of any event, calculated in \*days from the date of diagnosis (which will act as point zero on the timeline scale)
3. **STOP\_DATE**: The end date of the event is calculated in days from the date of diagnosis (which will act as point zero on the timeline scale).&#x20;
   * If the event occurs over time (e.g. a Treatment, ...) the STOP\_DATE column should have values.
   * If the event occurs at a time point (e.g. a Lab\_test, Imaging, ...) the STOP\_DATE is still mandatory, but the values should be blanks.
4. **EVENT\_TYPE**: the category of the event. You are free to define any type of event here. For several event types cBioPortal has column naming suggestions and for several events there are column names which have special effects.

{% hint style="info" %}
For more information about the Timeline columns, please visit the [official cBioPortal Documentation](https://docs.cbioportal.org/5.1-data-loading/data-loading/file-formats#timeline-data), and our [Clinical Timeline Setup](../../clinical-timeline-setup/) section
{% endhint %}

{% hint style="warning" %}
**Attention**: Some clinical attributes affect the timeline visualization. Please check the [Clinical Data](https://docs.cbioportal.org/5.1-data-loading/data-loading/file-formats#clinical-data) section for more information.
{% endhint %}
