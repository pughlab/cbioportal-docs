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

<table data-header-hidden><thead><tr><th></th><th></th><th width="87"></th><th width="113"></th><th width="134"></th><th></th><th></th><th></th><th></th><th></th></tr></thead><tbody><tr><td>PATIENT_ID</td><td>START_DATE</td><td>STOP_DATE</td><td>EVENT</td><td>DIAGNOSTIC_TYPE</td><td>RESULT</td><td>TREATMENT_CYCLE</td><td>TARGET_RESPONSE</td><td>NON_TARGET_RESPONSE</td><td>OVERALL_RESPONSE</td></tr><tr><td>ABC-01-0001</td><td>100</td><td></td><td>IMAGING</td><td>CT Scan</td><td>28</td><td>3</td><td>Partial response</td><td>NonCR/NonPD</td><td>Partial response</td></tr><tr><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td></tr></tbody></table>
