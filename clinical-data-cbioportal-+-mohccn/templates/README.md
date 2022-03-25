# Templates

MOHCCN has its required fields. cBioPortal has its required fields. Templates were created to merge the two sets of requirements. Since cBioPortal mandates that the clinical data is to be separated into clinical patient, samples and timeline files, where the data is categorized into several attribute types: patient, sample, and timeline. Users cannot put patient attributes into a sample file, there will be errors upon project import. The MOHCCN fields must follow this criteria to have a successful import. Thus, the _ICGC ARGO file_ categorization stated in the excel will not be followed here, although it is similar.&#x20;

**The MOHCCN field names are split up into the following files:**

* [ ] Patient File
* [ ] Sample File
* [ ] Timeline: Specimen
* [ ] Timeline: Treatment (general)
* [ ] Timeline: Treatment Medical Therapy
* [ ] Timeline: Treatment Radiation Therapy
* [ ] Timeline: Follow-up
