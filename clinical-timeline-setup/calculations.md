---
description: How to calculate the values for the START_DATE & STOP_DATE columns
---

# Calculations

## Dates Data Required

Small calculations for the START\_DATE and STOP\_DATE columns are required, as the expected value for these columns are \*days from the date of diagnosis (integer value)

#### To recap from what a [clinical timeline file must contain](what-is-it.md#timeline-column-requirements), the START\_DATE and STOP\_DATE columns are mandatory

* **START\_DATE**: the start point of any event, calculated in \*days from the date of diagnosis (which will act as point zero on the timeline scale)
* **STOP\_DATE**: The end date of the event is calculated in \*days from the date of diagnosis (which will act as point zero on the timeline scale)
  * If the event occurs over time (e.g. a Treatment, ...) the STOP\_DATE column should have values.&#x20;
  * If the event occurs at a time point (e.g. a Lab\_test, Imaging, ...) the STOP\_DATE is still mandatory, but the values should be blanks.&#x20;

{% hint style="info" %}
Therefore, you will need the patient's date of diagnosis to create any timeline data file. Depending on the type of timeline file you want to create, will require specific date data.
{% endhint %}

### START\_DATE column

If you want to create a specimen timeline, you will need the date of collection of each specimen. To calculate the START\_DATE value for a specimen:

For example, specimen ABC-01-0001-Xyz has\
&#x20;                              DATE\_OF\_COLLECTION = 2009-11-01\
&#x20;                              DATE\_OF\_DIAGNOSIS = 2009-06-15

DATE\_OF\_COLLECTION - DATE\_OF\_DIAGNOSIS = Days since the patient got diagnosed and the specimen was collected: \
`(2009-11-01) - (2009-06-15) = 139`

### STOP\_DATE column

If you want to calculate the STOP\_DATE for a treatment timeline data file, you will need the date the patient discontinued a specific treatment. To calculate the STOP\_DATE value for an end of a specific treatment:

For example, Patient ABC-01-0001 has ended their Nivolumab treatment: \
&#x20;                                 TREATMENT\_END\_DATE = 2011-04-15

TREATMENT\_END\_DATE - DATE\_OF\_DIAGNOSIS = Days since the patient ended their treatment:\
`(2011-04-15) - (2009-06-15) = 669`

{% hint style="warning" %}
For a specimen timeline, since it's an event that occurs at a single time point, the STOP\_DATE should be a blank. Do not put NA, N/A, or any variation of not applicable, unknown, or a space. Leave it blank.
{% endhint %}
