---
description: Some example projects containing timeline data from cBioPortal.org
---

# Example Reference Projects

## Example Projects

The following are example projects containing timeline data from cBioPortal.org. The project names links out to a patient in the project to show how a timeline is displayed on the user interface. The timeline data files for these timelines are also presented to help the user connect how the data is supposed to be formatted for project import. The actual imported files are to be in tab-delimited file format.

### [Glioma (MSK, Nature 2019)](https://www.cbioportal.org/patient?studyId=glioma\_msk\_2018\&caseId=IM-GBM-1)

This project contains a timeline for specimens. The following is the _data\_timeline\_specimen.txt_ file

| PATIENT\_ID | START\_DATE | STOP\_DATE | EVENT\_TYPE | SAMPLE\_ID     | NOTE             |
| ----------- | ----------- | ---------- | ----------- | -------------- | ---------------- |
| IM-GBM-1    | 5745        |            | SPECIMEN    | Patient-01-CSF | Sample Collected |
| IM-GBM-1    | 4242        |            | SPECIMEN    | Patient-01-T   | Sample Collected |
| IM-GBM-2    | 3876        |            | SPECIMEN    | Patient-02-CSF | Sample Collected |
| IM-GBM-2    | 3887        |            | SPECIMEN    | Patient-02-T   | Sample Collected |
| IM-GBM-3    | 2038        |            | SPECIMEN    | Patient-03-CSF | Sample Collected |
| IM-GBM-3    | 1909        |            | SPECIMEN    | Patient-03-T   | Sample Collected |
| IM-GBM-4    | 1911        |            | SPECIMEN    | Patient-04-CSF | Sample Collected |
| IM-GBM-4    | 1828        |            | SPECIMEN    | Patient-04-T   | Sample Collected |
| IM-GBM-5    | 828         |            | SPECIMEN    | Patient-05-CSF | Sample Collected |
| IM-GBM-5    | 0           |            | SPECIMEN    | Patient-05-T   | Sample Collected |
| IM-GBM-6    | 172         |            | SPECIMEN    | Patient-06-CSF | Sample Collected |
| IM-GBM-6    | 168         |            | SPECIMEN    | Patient-06-T   | Sample Collected |



### [Tumors with TRK fusions (MSK, Clin Cancer Res 2020)](https://www.cbioportal.org/patient?studyId=ntrk\_msk\_2019\&caseId=P-0002978)

This project contains timeline data for the patient's surgeries and treatments. The following is the _data\_timeline\_surgery.txt_, which contains several surgeries per patient (indicated in column SURGERY). The _data\_timeline\_treatment.txt_ file, contains several treatment types and subtypes

{% tabs %}
{% tab title="data_timeline_surgery.txt" %}


| PATIENT\_ID | START\_DATE | STOP\_DATE | EVENT\_TYPE | SURGERY   | SURGERY\_DETAILS                                                                                                          |
| ----------- | ----------- | ---------- | ----------- | --------- | ------------------------------------------------------------------------------------------------------------------------- |
| P-0007739   | 0           |            | SURGERY     | Surgery 1 | Outcome of First Surgery: Residual Disease                                                                                |
| P-0007911   | -5          |            | SURGERY     | Surgery 1 | Outcome of First Surgery: Residual Disease                                                                                |
| P-0002978   | 14          |            | SURGERY     | Surgery 1 | Outcome of First Surgery: Complete Resection                                                                              |
| P-0007552   | 0           |            | SURGERY     | Surgery 1 | Outcome of First Surgery: Residual Disease (very soon after surgery needed re-resection and wedge resection of lung mets) |
| P-0007911   | 5235        |            | SURGERY     | Surgery 2 |                                                                                                                           |
| P-0002978   | 2553        |            | SURGERY     | Surgery 2 |                                                                                                                           |
| P-0007552   | 184         |            | SURGERY     | Surgery 2 |                                                                                                                           |
| P-0002978   | 2715        |            | SURGERY     | Surgery 3 |                                                                                                                           |
| P-0007552   | 336         |            | SURGERY     | Surgery 3 |                                                                                                                           |
| P-0007552   | 469         |            | SURGERY     | Surgery 4 |                                                                                                                           |
{% endtab %}

{% tab title="data_timeline_treatment.txt" %}
| PATIENT\_ID | START\_DATE | STOP\_DATE | EVENT\_TYPE | TREATMENT\_TYPE   | SUBTYPE                 | AGENT                              | ONGOING\_TREATMENT | BEST\_RESPONSE\_THER | REASON\_TX\_DISCON | SITE\_OF\_RAD\_THERA |
| ----------- | ----------- | ---------- | ----------- | ----------------- | ----------------------- | ---------------------------------- | ------------------ | -------------------- | ------------------ | -------------------- |
| P-0007739   | 15          | 365        | TREATMENT   | Medical Therapy   | Line 1 Chemo Indication | FUDR-HAI\_Irinotecan               | Yes                | No Imaging           | Death              |                      |
| P-0003670   | 136         | 195        | TREATMENT   | Medical Therapy   | Line 1 Chemo Indication | Carboplatin\_Paclitaxel\_Erlotinib | No                 | PR                   | Intolerance        |                      |
| P-0002978   | 2298        | 2359       | TREATMENT   | Medical Therapy   | Line 1 Chemo Indication | Vinorelbine                        | No                 | POD                  | POD                |                      |
| P-0007739   | 379         | 570        | TREATMENT   | Medical Therapy   | Line 2 Chemo Indication | HAI-FUDR\_XELOX                    | No                 | SD                   | Intolerance        |                      |
| P-0003670   | 226         | 532        | TREATMENT   | Medical Therapy   | Line 2 Chemo Indication | Paclitaxel\_Erlotinib              | No                 | PR                   | Intolerance        |                      |
| P-0002978   | 2390        | 2481       | TREATMENT   | Medical Therapy   | Line 2 Chemo Indication | Carboplatin\_Paclitaxel            | No                 | SD                   | Completed Therapy  |                      |
| P-0007739   | 596         | 1142       | TREATMENT   | Medical Therapy   | Line 3 Chemo Indication | HAI-FUDR\_Oxaliplatin\_Irinotecan  | No                 | CR                   | CR                 |                      |
| P-0003670   | 560         | 3301       | TREATMENT   | Medical Therapy   | Line 3 Chemo Indication | Erlotinib                          | No                 | SD                   | Other              |                      |
| P-0002978   | 2821        | 2947       | TREATMENT   | Medical Therapy   | Line 3 Chemo Indication | Doxorubicin                        | No                 | PR                   | Other              |                      |
| P-0003670   | 3837        | 4234       | TREATMENT   | Medical Therapy   | Line 4 Chemo Indication | Pemetrexed\_Bevacizumab\_Erlotinib | No                 | SD                   | POD                |                      |
| P-0002978   | 3081        | 3210       | TREATMENT   | Medical Therapy   | Line 4 Chemo Indication | Crizotinib                         | No                 | SD                   | POD                |                      |
| P-0003670   | 4299        | 4668       | TREATMENT   | Medical Therapy   | Line 5 Chemo Indication | Nivolumab                          | No                 | SD                   | POD                |                      |
| P-0002978   | 3234        | 3526       | TREATMENT   | Medical Therapy   | Line 5 Chemo Indication | Entrectinib                        | No                 | PR                   | POD                |                      |
| P-0003670   | 4717        | 5221       | TREATMENT   | Medical Therapy   | Line 6 Chemo Indication | Larotrectinib                      | Yes                | SD                   | Intolerance        |                      |
| P-0002978   | 3536        | 3561       | TREATMENT   | Medical Therapy   | Line 6 Chemo Indication | Larotrectinib                      | No                 | POD                  | POD                |                      |
| P-0002978   | 3659        | 3837       | TREATMENT   | Medical Therapy   | Line 7 Chemo Indication | Entrectinib\_Trametinib            | No                 | PR                   | POD                |                      |
| P-0002978   | 3908        | 3912       | TREATMENT   | Medical Therapy   | Line 8 Chemo Indication | LOXO-195                           | No                 | POD                  | Death              |                      |
| P-0003670   | 3275        | 3303       | TREATMENT   | Radiation Therapy | RADIATION THERAPY 1     |                                    |                    |                      |                    | mediastinum          |
| P-0002978   | 62          | 106        | TREATMENT   | Radiation Therapy | RADIATION THERAPY 1     |                                    |                    |                      |                    | Parotid              |
| P-0003670   | 4321        | 4398       | TREATMENT   | Radiation Therapy | RADIATION THERAPY 2     |                                    |                    |                      |                    | hilum\_SRSbrain      |
| P-0002978   | 3569        | 3575       | TREATMENT   | Radiation Therapy | RADIATION THERAPY 2     |                                    |                    |                      |                    | chest wall           |
| P-0002978   | 3607        | 3612       | TREATMENT   | Radiation Therapy | RADIATION THERAPY 3     |                                    |                    |                      |                    | Right lung           |
{% endtab %}
{% endtabs %}

