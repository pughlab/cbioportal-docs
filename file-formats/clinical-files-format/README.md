# Clinical Files Format

## Main Clinical Files

### Consistent SAMPLE\_ID&#x20;

{% hint style="warning" %}
Having consistent sample ID's throughout the genomic and clinical files is extremely important. With a small tiny difference of just one character, for instance, a dash instead of an underscore (that is referring to the same sample) for any of the import files, there will be errors upon project import.
{% endhint %}

### Clinical Samples File

Clinical data in cBioPortal is flexible. The minimal required file required for a project import is a clinical samples fil&#x65;_._ This file is THE mapping link between genomic data and clinical data by the common sample ID. However, having more data than just the patient ID and sample ID data is always best, as it will make your project relevant and provide a complete patient profile.&#x20;

With the application of the [MOHCCN Clinical Data Standards](../../clinical-data-cbioportal-+-mohccn/), consisting of mCODE & ARGO data standards, there is a [clinical samples template](../../clinical-data-cbioportal-+-mohccn/templates/sample-file.md) along with cBioPortal required fields for your reference.

### Text File to User Interface

The acceptable clinical file format for cBioPortal import is a tab-delimited file. The clinical samples data will be displayed on the user-interface via the patient view header's second line, where it lists all the samples associated with a patient. When hovering over a sample ID, a text box will be displayed listing all the sample details indicated in the clinical samples file. Additionally, the data is also displayed in the _Clinical Data_ tab under the Samples section.

### Patient attributes vs. Sample attributes

In reality, having both a clinical patients and samples file is best to provide a complete project. Please categorize the clinical data properly, as cBioportal will give errors when incorrect data headers are placed in the wrong file.&#x20;

Any data that concerns the patient, the person’s characteristics, will be a patient attribute. Any data that is about the sample and its characteristics, will be a sample attribute.

* For example, data such as `AGE`, `GENDER`, `RACE`, `CENTRE` (place where patient is undergoing treatment), `DATE_OF_DIAGNOSIS`, etc are all patient attributes - as it pertains to the patient.&#x20;
* Data such as `CANCER_TYPE`_,_ `CANCER_TYPE_DETAILED`, `ONCOTREE_CODE`, `SAMPLE_TYPE`, `SAMPLE_CLASS`, etc are sample attributes and goes in the clinical samples file.&#x20;

The `ONCOTREE_CODE` column header is a way to categorize and communicate cancer types in a standardized manner. For more detailed information, please refer to the [OncoTree code section](clinical-sample-file-oncotree-code.md).

In reference to the MOHCCN Clinical data standards, the patient attributes would be the “Donor” fields (\*except “PRIMARY\_SITE” as cBioPortal deems this type of data as a sample attribute). All the “Sample registration”, “Specimen”, and “Primary Diagnosis” schemas would be the sample attributes. All these MOHCCN fields are already split up into the appropriate [cBio-MOHCCN ready](../../clinical-data-cbioportal-+-mohccn/templates/) blue tabs in the downloadable excel workbook provided.

## Clinical Timelines

If the user has additional clinical data they would like to import, cBioPortal suggests to display them as clinical timeline files. Clinical timeline files are also tab-delimited text files, however the data will be represented on the patient's _Summary_ tab as a timeline data point/track. The timeline details (such as what type of treatment, drug name, type of radiation, etc.) will be displayed in a text box when hovering over the specific timeline point/track. Additionally, the timeline details will also be displayed on the patient's _Clinical Data_ tab under the header _Timeline Data._

In order to have a successful timeline, there must be dates data. One cannot create a cBioportal timeline without any dates data. The date of diagnosis is a must have data point, as it will act as point zero on the clinical timeline scale. You will use the date of diagnosis to calculate any type of timeline, as the start point (`START_DATE`) is calculated in _DAYS._

{% hint style="info" %}
For more information about how to set up clinical timeline files, please refer to the [Clinical Timeline Setup](../clinical-timeline-setup/what-is-it.md) section or the official cBioportal documentation's [Timeline Data](https://docs.cbioportal.org/5.1-data-loading/data-loading/file-formats#timeline-data) section
{% endhint %}

If you are going to apply the MOHCCN clinical data standards, there are [templates](../../clinical-data-cbioportal-+-mohccn/templates/timeline-specimen.md) for each schema, their affiliated fields, and the required cBioPortal fields under the [Clinical Data: cBioPortal + MOHCCN section](../../clinical-data-cbioportal-+-mohccn/) of this documentation.

### Dates and Formatting

There is no requirement by cBioPortal for the user to import the actual dates data for their project. However, if one wishes to do so, it is allowed. If a user wanted to create clinical timeline files to create a timeline visualization on a patient’s profile view, dates are required to do the calculation for the START\_DATE & STOP\_DATE columns. The values in these two columns are integer values for the number of days. The calculation can be done on the side and the final calculated integer value (days) would be what is recorded in the clinical timeline file and imported. The OS\_MONTHS and DFS\_MONTHS columns in the clinical patients file also require dates to calculate the months, an integer value. Again, this can be calculated on the side. The actual dates to calculate these column values, do not need to be imported.

#### Formatting

If the study’s PI wants to import dates and have granted permission to do so, for consistency the preferred date format would be the international standard ISO 8601, in the extended format. The ISO 8601 - extended format is YYYY-MM-DD. It is important to communicate dates in an international standard as it allows all collaborators from everywhere to easily interpret the date data in an unambiguous way. IONOs also refers to the ISO 8601 as the international standard for the date format. [https://www.ionos.ca/digitalguide/websites/web-development/iso-8601/](https://www.ionos.ca/digitalguide/websites/web-development/iso-8601/)

