# Templates

The MOHCCN data standard has its required fields. cBioPortal has its required fields. Templates were created to merge the two sets of requirements. Since cBioPortal mandates that the clinical data is to be separated into clinical patient, samples and timeline files, where the data is categorized into several attribute types: patient, sample, and timeline. Users cannot put patient attributes into a sample file, there will be errors upon project import. The MOHCCN fields must follow this criteria to have a successful import. Thus, the _ICGC ARGO file_ categorization stated in the excel will not be followed here, although it is similar.&#x20;

**The MOHCCN field names are split up into the following files:**

* [ ] Patient File
* [ ] Sample File
* [ ] Timeline: Specimen
* [ ] Timeline: Treatment (general)
* [ ] Timeline: Treatment Medical Therapy
* [ ] Timeline: Treatment Radiation Therapy
* [ ] Timeline: Follow-up

### cBioPortal MOHCCN Clinical Fields Template

{% file src="../../.gitbook/assets/cBioportal_MOHCCN_Clinical_Fields_updated_April062022.xlsx" %}
The downloadable excel file including the MOHCCN data standard and associated templates
{% endfile %}

{% hint style="warning" %}
The template is in excel for the user's ease in filling out the data. However, for the actual cBioPortal project import, the file is to be in tab-delimited format. Please do not include empty columns or extra spaces, as these will give errors upon import.
{% endhint %}

