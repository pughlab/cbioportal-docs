# Clinical Sample File: OncoTree Code

## OncoTree Code?

[OncoTree](http://oncotree.mskcc.org) is an open-source ontology for categorizing and standardizing cancer type diagnoses. This ontology was developed by [Memorial Sloan Kettering Cancer Center](https://www.mskcc.org) (MSK). Each diagnosis is assigned a unique OncoTree code (an abbreviation of the full cancer type diagnosis name).

In cBioPortal, we use the OncoTree codes to help distinguish the specific cancer type of the patient. The clinical samples section of the cBioPortal documentation mentions "`CANCER_TYPE"` and “`CANCER_TYPE_DETAILED`” fields. However, there is no mention of an “`ONCOTREE_CODE`” field in the documentation. On the _cbioportal.org_ website, projects have this “Oncotree Code” field displayed. Thus, to implement consistency in our projects and to have all the relevant information displayed, we are incorporating the “`ONCOTREE_CODE`” field in the clinical samples file.

## Categorizing the Cancer Type Information

The “`CANCER_TYPE`” field would be the general cancer type name. The name in the base level after ‘Tissue’ on the Oncotree Map

* For example: “Lung”

The “`CANCER_TYPE_DETAILED`” field would be the name of the specific cancer type (going down the Oncotree map)

* For example: “Poorly Differentiated Non-Small Cell Lung Cancer”

The “`ONCOTREE_CODE`” field would be the acronym of the Cancer Type Detailed name in the “`CANCER_TYPE_DETAILED`” field

* For example: “NSCLCPD”

### OncoTree code example

![OncoTree code example: CANCER\_TYPE = "Lung"; CANCER\_TYPE\_DETAILED = "Poorly Differentiated Non-Small Cell Lung Cancer"; ONCOTREE\_CODE = "NSCLCPD"](../../.gitbook/assets/oncotree\_code\_example.png)



