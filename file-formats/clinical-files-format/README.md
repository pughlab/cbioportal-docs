# Clinical Files Format

## Main Clinical Files

### Clinical Samples File

Clinical data in cBioPortal is flexible. The minimal required file required for a project import is a clinical samples file_._ This file is THE mapping link between genomic data and clinical data by the common sample ID. However, having more data than just the patient ID __ and __ sample ID data is always best, as it will make your project relevant and provide a complete patient profile.&#x20;

#### Consistent SAMPLE\_ID&#x20;

{% hint style="warning" %}
Having consistent sample ID's throughout the genomic and clinical files is extremely important. With a small tiny difference of just one character, for instance, a dash instead of an underscore (that is referring to the same sample ID) for any of the import files, there will be errors upon project import.
{% endhint %}

### Text File to User Interface

The acceptable clinical file format for cBioPortal import is a tab-delimited file. The clinical samples data will be displayed on the user-interface via the patient view header's second line, where it lists all the samples associated with a patient. When hovering over a sample ID, a text box will be displayed listing all the sample details indicated in the clinical samples file. Additionally, the data is also displayed in the _Clinical Data_ tab under the Samples section.

### Patient attributes vs. Sample attributes

In reality, having both a clinical patients and samples file is best to provide a complete project. Please categorize the clinical data properly, as cBioportal will give errors when incorrect data headers are placed in the wrong file.&#x20;

* For example, data such as `AGE`, `GENDER`, `RACE`, `CENTRE` (place where patient is undergoing treatment), `DATE_OF_DIAGNOSIS`, etc are all patient attributes - as it pertains to the patient.&#x20;
* Data such as `CANCER_TYPE`_,_ `CANCER_TYPE_DETAILED`, `ONCOTREE_CODE`, `SAMPLE_TYPE`, `SAMPLE_CLASS`, etc are sample attributes and goes in the clinical samples file.&#x20;



## Clinical Timelines

If the user has additional clinical data they would like to import, cBioPortal suggests to display them as clinical timeline files. Clinical timeline files are also tab-delimited text files, however the data will be represented on the patient's _Summary_ tab as a timeline data point/track. The timeline details (such as what type of treatment, drug name, type of radiation, etc.) will be displayed in a text box when hovering over the specific timeline point/track. Additionally, the timeline details will also be displayed on the patient's _Clinical Data_ tab under the header _Timeline Data._

In order to have a successful timeline, there must be dates data. One cannot create a cBioportal timeline without any dates data. The date of diagnosis is a must have data point, as it will act as point zero on the clinical timeline scale. You will use the date of diagnosis to calculate any type of timeline, as the start point (`START_DATE`) is calculated in _DAYS._

__

__

