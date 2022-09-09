---
description: General Treatment timeline file
---

# Timeline: Treatment

## Timeline: Treatment Headers

These are the field names under the _ICGC ARGO File_ category 'Treatment'

| **PATIENT\_ID** | **START\_DATE** | **STOP\_DATE** | **EVENT\_TYPE** | _<mark style="color:blue;">TREATMENT\_TYPE</mark>_ | _<mark style="color:blue;">SUBTYPE</mark>_ | SUBMITTER\_TREATMENT\_ID | SUBMITTER\_PRIMARY\_DIAGNOSIS\_ID | IS\_PRIMARY\_TREATMENT | TREATMENT\_SETTING | TREATMENT\_INTENT | RESPONSE\_TO\_TREATMENT |
| --------------- | --------------- | -------------- | --------------- | -------------------------------------------------- | ------------------------------------------ | ------------------------ | --------------------------------- | ---------------------- | ------------------ | ----------------- | ----------------------- |
| ABC-01-0001     | 10              | 26             | TREATMENT       | Line of Therapy                                    | First Line                                 |                          |                                   | Yes                    |                    | Curative          |                         |
| ABC-01-0001     | 31              | 64             | TREATMENT       | Line of Therapy                                    | Second Line                                |                          |                                   | Yes                    |                    | Curative          |                         |
| ABC-01-0050     | 6               | 22             | TREATMENT       | Line of Therapy                                    | First Line                                 |                          |                                   | No                     |                    | Curative          |                         |

### Legend

Black and bold font are mandatory cBioportal headers

* **PATIENT\_ID** = "submitter\_donor\_id"
* **START\_DATE** = "treatment\_start\_interval"
* **STOP\_DATE** = "treatment\_duration"
* **EVENT\_TYPE** = 'TREATMENT'

#### cBioPortal suggested columns in _<mark style="color:blue;">blue italics</mark>_:

* _<mark style="color:blue;">TREATMENT\_TYPE</mark>_: Since this is the general treatment timeline file, this header can be used to generalize the group of treatment, ie value: 'Line of Therapy'. This will create an indented track within the Treatment section of the timeline visualization on cBioPortal.
* _<mark style="color:blue;">SUBTYPE</mark>_: Since this is the general treatment timeline file, this header can be used to further categorize the treatment type, ie values: "First Line", "Second Line", "Third Line", etc. This will create a further indented sub-category within the above treatment type name on the timeline visualization.
* <mark style="color:red;">Special</mark>: When using the _<mark style="color:blue;">AGENT</mark>_ and _<mark style="color:blue;">SUBTYPE</mark>_ columns, each agent and subtype will be split into its own track.



{% hint style="info" %}
For more information about the Timeline columns, please visit the [official cBioPortal Documentation](https://docs.cbioportal.org/5.1-data-loading/data-loading/file-formats#timeline-data), and our [Clinical Timeline Setup](../../file-formats/clinical-timeline-setup/) section
{% endhint %}

