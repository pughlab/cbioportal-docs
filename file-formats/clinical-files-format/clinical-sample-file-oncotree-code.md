# Clinical Sample File: OncoTree Code

## OncoTree Code?

[OncoTree](http://oncotree.mskcc.org/) is an open-source ontology for categorizing and standardizing cancer type diagnoses. This ontology was developed by [Memorial Sloan Kettering Cancer Center](https://www.mskcc.org/) (MSK). Each diagnosis is assigned a unique OncoTree code (an abbreviation of the full cancer type diagnosis name).

In cBioPortal, we use the OncoTree codes to help distinguish the specific cancer type of the patient. The clinical samples section of the cBioPortal documentation mentions "`CANCER_TYPE"` and “`CANCER_TYPE_DETAILED`” fields. However, there is no mention of an “`ONCOTREE_CODE`” field in the documentation. On the _cbioportal.org_ website, projects have this “Oncotree Code” field displayed. Thus, to implement consistency in our projects and to have all the relevant information displayed, we are incorporating the “`ONCOTREE_CODE`” field in the clinical samples file.

## Categorizing the Cancer Type Information

The “`CANCER_TYPE`” field would be the general cancer type name aka tissue type. The name in the base level after ‘Tissue’ on the Oncotree Map

* For example: “Lung”

The “`CANCER_TYPE_DETAILED`” field would be the name of the specific cancer type (going down the Oncotree map)

* For example: “Poorly Differentiated Non-Small Cell Lung Cancer”

The “`ONCOTREE_CODE`” field would be the acronym of the Cancer Type Detailed name in the “`CANCER_TYPE_DETAILED`” field

* For example: “NSCLCPD”

### OncoTree code example

![Figure 1: A user can search for their cancer type, specific cancer type name or the oncotree code in the search field. OncoTree code example: CANCER\_TYPE = "Lung" (being the tissue type); CANCER\_TYPE\_DETAILED = "Poorly Differentiated Non-Small Cell Lung Cancer" (being the specific cancer type name); ONCOTREE\_CODE = "NSCLCPD" (the oncotree code for this specific cancer type name). The cancer type detailed and oncotree code is highlighted in red font for the user.](../../.gitbook/assets/Oncotree\_code\_example.png)
