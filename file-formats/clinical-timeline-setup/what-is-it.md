---
description: Clinical timelines explained
---

# What is it?

## What is a clinical timeline?

To have a full clinical data set on cBioPortal, it is suggested that the user includes this data as clinical timeline files. With clinical timeline data, a visualization of this data will be displayed on the patient view (_Summary_ tab). This allows the user to visualize the various time points of treatments, surgeries, samples of a patient since diagnosis. For each timeline track, the user can see details of that event by hovering over it, in which an information popup box will be displayed. The timeline data will also be displayed in the _Clinical Data_ tab, within the _Timeline Data_ section. Each additional timeline file will create a separate timeline track. Each timeline file has its own event type, which will generate a timeline for said event. An event type could be anything. Examples of event types: Specimen, Surgery, Treatment, Lab Test, etc. Several event types have column naming suggestions with special effects. Each event type would need its own clinical timeline data file and subsequently its own meta file.

{% hint style="info" %}
For more [Timeline Data information](https://docs.cbioportal.org/5.1-data-loading/data-loading/file-formats#timeline-data) please refer to the official cBioPortal documentation.
{% endhint %}

{% hint style="warning" %}
**Attention**: Some clinical attributes affect the timeline visualization. Please check the [Clinical Data section](https://docs.cbioportal.org/5.1-data-loading/data-loading/file-formats#clinical-data) in the official cBioPortal documentation for more information
{% endhint %}

## Timeline Column Requirements

Regardless of which event type is to be created, all timeline data files must contain these 4 columns in this order (left to right):

1. &#x20;**PATIENT\_ID**: the patient ID from the dataset
2. **START\_DATE**: the start point of any event, calculated in \*days from the date of diagnosis (which will act as point zero on the timeline scale)
3. **STOP\_DATE**: The end date of the event is calculated in days from the date of diagnosis (which will act as point zero on the timeline scale). If the event occurs over time (e.g. a Treatment, ...) the STOP\_DATE column should have values. If the event occurs at a time point (e.g. a Lab\_test, Imaging, ...) the STOP\_DATE is still mandatory, but the values should be blanks.
4. **EVENT\_TYPE**: the category of the event. You are free to define any type of event here. For several event types cBioPortal has column naming suggestions and for several events there are column names which have special effects. See event types for more information.

{% hint style="warning" %}
Having the DATE\_OF\_DIAGNOSIS data is extremely important and key to creating a clinical timeline file. As well as having DATES data for any type of event. You do not need to import the actual dates data into cBioPortal. However, you need to have this information in order to calculate the integer values for the **START\_DATE** and **STOP\_DATE** columns, which are mandatory.
{% endhint %}
