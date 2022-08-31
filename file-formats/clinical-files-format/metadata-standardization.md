---
description: >-
  Standardizing the clinical metadata through the cBioPortal's clinical hashtag
  (#) rows
---

# MetaData Standardization

## cBioPortal Metadata Headers

This is implemented by those first two out of the four hash tag (#) rows required in the clinical patients and clinical samples file. Only these two clinical files require these four # rows. The clinical timeline files (if applicable) do not require these special # rows.

* This is pertaining to the first two hash tag rows (#)
  * The clinical metadata format displayed on cBioPortal is dependent on these two rows
  * The content of the first two # rows is the same as the main header row
    * The main header row (for example, the 5th row in the example image) is required to be database type headers (all capitalized letters, no spaces, using underscores)
  * Each word is to be fully spelled out (instead of various types of abbreviations/database type header names etc.)
  * Headers to be in Title Case (major words are capitalized, and most minor words are lowercase)
    * For example: “Overall Survival Status”
    * For example: “Type of Breast Surgery”
  * However, it is understandable for certain acronyms to stay as acronyms such as “HER2”, “ER”, “MLH1”, “Patient ID”, etc., so those can remain as acronyms

![Figure 2: Example of a clinical patient file. Source: cBioPortal.org's Documentation](../../.gitbook/assets/cbioportal\_metadata\_headers.png)

![Figure 3: Example of how the meta-data would look like after project import of the clinical patient file (figure 2). The first two hash tag rows from the clinical patient file (figure 2) is imported as the entries under the "Attribute" header. The values from rows 6 onwards (figure 2) are the values that are displayed on the right hand side of this image.](../../.gitbook/assets/Results\_of\_metadata\_on\_user\_interface.png)



