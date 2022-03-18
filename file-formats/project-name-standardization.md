---
description: All begins with the meta_study.txt file
---

# Project Name Standardization

## Project Details

The general information of a cBioPortal project are described in a mandatory file, the [_meta\_study.txt_](https://docs.cbioportal.org/5.1-data-loading/data-loading/file-formats#meta-file) file. Within this file is where the project's name, project description, what reference genome build was used, the type of cancer the project is based on, etc. For all the available field options in the meta\_study.txt file, please refer to the official cBioPortal's documentation.

### Common meta\_study fields used

| cancer\_study\_identifier:   <- usually the projects acronym                                                                                                          |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name:   <- the [naming structure](project-name-standardization.md#the-naming-structure-of-the-project-name-is-acronym-top-level-oncotree-concept-pi-centre) goes here |
| description:   <- description of what the project is about                                                                                                            |
| type\_of\_cancer:   <- The cancer type abbreviation, e.g., "brca". Please use the [OncoTree Code](http://oncotree.mskcc.org/#/home)                                   |
| reference\_genome:   <- hg19 OR hg38                                                                                                                                  |
| add\_global\_case\_list: true                                                                                                                                         |

### Name field

For a better user experience, we ask that each project import to follow a naming structure when filling out the details in the meta\_study.txt file. By following this naming structure, the user can quickly grasp what a project is about and find what they are looking for.&#x20;

### The naming structure of the project Name is “<mark style="color:red;">ACRONYM</mark>: <mark style="color:purple;">Top-level-OncoTree</mark> - <mark style="color:green;">Concept</mark> (<mark style="color:orange;">PI</mark>, <mark style="color:blue;">Centre</mark>)”

1. <mark style="color:red;">ACRONYM</mark> <- if your study has an acronym for it
2. <mark style="color:purple;">Top-level-OncoTree</mark> <- the Cancer Type Detailed Name
3. <mark style="color:green;">Concept</mark> <- Xenograft? Cell line? Clinical Trial? Landscape of cohorts? etc
4. <mark style="color:orange;">PI</mark> <- Main Principal Investigator of the project
5. <mark style="color:blue;">Centre</mark> <- which centre generated this data





