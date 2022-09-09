---
description: Creating new clinical timelines
---

# Additional Clinical Tracks

cBioPortal is very flexible, if you have additional information that you would like to include in your study, and display it as a timeline, you can. Column "EVENT\_TYPE" can be anything.&#x20;

Each track on the timeline is based on an event type.

{% hint style="info" %}
cBioPortal already have some event types that are predefined and have special effects when used. Please see the [event types under Clinical Tracking Order](https://docs.cbioportal.org/file-formats/#clinical-track-ordering) for more information on the official cBioPortal documentation. For example, it can be "Lab\_test", "Imaging", etc. Also, for these predefined event types, there are also some suggested predefined column names that the user can use.
{% endhint %}

#### Example: "Imaging" Event

| PATIENT\_ID | START\_DATE | STOP\_DATE | EVENT   | DIAGNOSTIC\_TYPE | RESULT | TREATMENT\_CYCLE | TARGET\_RESPONSE | NON\_TARGET\_RESPONSE | OVERALL\_RESPONSE |
| ----------- | ----------- | ---------- | ------- | ---------------- | ------ | ---------------- | ---------------- | --------------------- | ----------------- |
| ABC-01-0001 | 100         |            | IMAGING | CT Scan          | 28     | 3                | Partial response | NonCR/NonPD           | Partial response  |
|             |             |            |         |                  |        |                  |                  |                       |                   |
