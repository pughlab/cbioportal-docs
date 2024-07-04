# cBioportal Import Files Directory

Now that you have all your genomic and clinical data files in the proper cBioportal formats, they all need to be located in one directory, which we call the staging or working directory. All your genomic and clinical data files, are called your data files and should have the prefix "data\_" in the filename. For each data file, there is an associated metadata file called meta files, which needs to have the prefix "meta\_". The meta files describe and list the filename for the specific data type.&#x20;

## Typical cBioportal Staging Directory

<div data-full-width="false">

<figure><img src="../.gitbook/assets/image (1).png" alt="" width="563"><figcaption><p>A typical cBioportal staging/working directory</p></figcaption></figure>

</div>

There are specific fields and values that cBioportal expects during import, for every different data type. Please refer to the official cBioportal documentation website for more information. The following are quick links to the meta file data for the common data types. On the official cBioportal documentation there are information and examples on all the different data types that a user can import into cBioportal.

### Meta Files Quick Links:

* **Clinical Patient and Sample** Data meta files (they each have a different value for the "datatype" and "data\_filename" fields) : [https://docs.cbioportal.org/file-formats/#meta-files](https://docs.cbioportal.org/file-formats/#meta-files)
* **Clinical Timeline** Data meta files: [https://docs.cbioportal.org/file-formats/#meta-file-12](https://docs.cbioportal.org/file-formats/#meta-file-12)
* **Mutation** Data meta file: [https://docs.cbioportal.org/file-formats/#meta-file-7](https://docs.cbioportal.org/file-formats/#meta-file-7)
* **Seg** Data meta file: [https://docs.cbioportal.org/file-formats/#meta-file-5](https://docs.cbioportal.org/file-formats/#meta-file-5)
* **Structural Variant** meta file: [https://docs.cbioportal.org/file-formats/#meta-file-10](https://docs.cbioportal.org/file-formats/#meta-file-10)
* **CNA** - discrete (wide format) meta file: [https://docs.cbioportal.org/file-formats/#wide-format](https://docs.cbioportal.org/file-formats/#wide-format)

