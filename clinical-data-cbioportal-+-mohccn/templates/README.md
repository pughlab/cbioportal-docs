# Templates

The MOHCCN data standard has its required fields. cBioPortal has its required fields. Templates were created to merge the two sets of requirements. Since cBioPortal mandates that the clinical data is to be separated into clinical patient, samples and timeline files, where the data is categorized into several attribute types: patient, sample, and timeline. Users cannot put patient attributes into a sample file, there will be errors upon project import. The MOHCCN fields must follow this criteria to have a successful import. Thus, the _ICGC ARGO File_ categorization stated in the Data Standard will not be followed here, although it is similar.&#x20;

**The MOHCCN fields are split up into the following files:**

* [ ] Patients
* [ ] Samples
* [ ] Timeline: Specimen
* [ ] Timeline: Treatment Medical Therapy
* [ ] Timeline: Treatment Radiation Therapy
* [ ] Timeline: Surgery
* [ ] Timeline: Follow-up
* [ ] Timeline: Relapse
* [ ] Timeline: Biomarker

## cBioPortal MOHCCN Clinical Fields Template

### MOHCCN Standard Sept 2022 version

{% file src="../../.gitbook/assets/cBioportal_MOHCCN_Standard_Clinical_Fields_Template_updated_Sept202022.xlsx" %}
A downloadable excel template of the MOHCCN Standard with cBioPortal required and suggested fields
{% endfile %}

### MOHCCN Standard Feb 2023 version (V2)

{% file src="../../.gitbook/assets/cBioportal_MOHCCN_Standard_Clinical_Fields_Template_updated_Feb2023version.xlsx" %}
A downloadable excel template of the MOHCCN Standard with cBioPortal required and suggested fields
{% endfile %}

### MOHCCN Standard May 2024 version (V3)

{% file src="../../.gitbook/assets/cBioportal_MOHCCN_Standard_Clinical_Fields_Template_V3_May2024.xlsx" %}
A downloadable excel template of the MOHCCN Standard mapped with cBioPortal required and suggested fields
{% endfile %}

### MOHCCN Standard Sept 2024 version (V3.1)

{% file src="../../.gitbook/assets/cBioportal_MOHCCN_Standard_Clinical_Fields_Template_V3.1_Sept2024.xlsx" %}
A downloadable excel template of the MOHCCN Standard mapped with cBioPortal required and suggested fields
{% endfile %}

{% hint style="warning" %}
The template is in excel for the user's ease in filling out the data. However, for the actual cBioPortal project import, the file is to be in tab-delimited format. Please do not include empty columns or extra spaces, as these will give errors upon import.
{% endhint %}
