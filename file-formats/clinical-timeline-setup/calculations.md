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

### Consistent Date Format

{% hint style="warning" %}
It is very important to have consistent date entry formats.&#x20;
{% endhint %}

For consistency the preferred date format would be the international standard ISO 8601, in the extended format. The ISO 8601 - extended format is **YYYY-MM-DD**. It is important to communicate dates in an international standard as it allows all collaborators from everywhere to easily interpret the date data in an unambiguous way. IONOs also refers to the ISO 8601 as the international standard for the date format. [https://www.ionos.ca/digitalguide/websites/web-development/iso-8601/](https://www.ionos.ca/digitalguide/websites/web-development/iso-8601/)

Always check to see if the resulting days have negative values (which suggest that there's a mix up in the encoding of month and day). Be careful of the order of the dates in the calculation (ie the earlier date is subtracted from the later date will give you a negative value). Unless, a prior treatment timeline is the intention (ie treatments done prior to the date of diagnosis).&#x20;

To calculate the day value (integer value), this can be easily done in excel, only if the data type is set correctly.

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

## Tutorials

For reference on how to do this, you can refer to the following excel tutorials that explains date conversion and calculations.

**Date Conversion (setting up data type correctly) in excel**:

{% embed url="https://www.youtube.com/watch?v=FErqhZl1Vds" %}
A tutorial on how to convert text to date values in excel and other tips
{% endembed %}

**Date Calculations in excel:**

{% embed url="https://www.youtube.com/watch?v=XJ96nwXpa7Y" %}
A tutorial on how to calculate an integer value from two dates in excel
{% endembed %}

* Another resource on how to calculate an integer value from two dates: [Calculating the number of days between two dates in excel](https://ecampusontario.pressbooks.pub/businessmath/chapter/calculating-the-number-of-days-between-two-dates-in-ms-excel/)
