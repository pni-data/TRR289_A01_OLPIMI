# TRR289 OLPIMI

## ℹ️ Information
*This repository is the Github sibling of the corresponding [DataLad](https://www.datalad.org/) dataset, i.e. it **does not** contain the data itself.*
The GitHub sibling, nevertheless, provides insights into the general data structure (directory tree, filenames) and serves as a starting point to download, share and discuss the dataset.
 Data is in BIDS format and may include behavioral, questionnaire and derivative data, too.
Data is stored in a special S3 remote provided by [Coscine](https://coscine.rwth-aachen.de/) and can't be downloaded without the dataset specific secret token.
Token is available at project Z03 for members of TRR289 and collaborators upon reasonable request.

See `dataset_description.json` for project related meta-data.

## ⬇️ How to download dataset

#### 1. Install it with DataLad based on the github handle
This does not download the actual data, only the gin-annex "skeleton".
```bash
datalad install -s git@github.com:pni-data/<dataset_name>.git <dataset_name>
datalad siblings configure -s origin --publish-depends coscine-rds-s3
```
#### 2. Set up the security token to access the actual data
Token is available at project Z03 for members of TRR289 and collaborators upon reasonable request.
```bash
export AWS_ACCESS_KEY_ID="XXXXX-XXXX-XXXX-XXXX-XXXX"
export AWS_SECRET_ACCESS_KEY="XXXXXXXX"
```

#### 2. Change to the dataset directory and download the file(s) you want
You can selectively download what you need (e.g. derivatives only).
```bash
cd <dataset_name>
datalad get <path/to/file*>
```

See our [documentation](https://github.com/pni-data/.github/blob/master/profile/README.md) for more detail.


Comments added by the SFB289 Z03 project coordinators
====================================================================



General Comments
--------------------------------------------------------------------
ToDo link detailed information about the dataset
eg: This dataset was acquired by the team of the TRR/SFB289 A01 project. It includes 112 subjects with the common sequences within the SFB289 project, namely a high resolution T1w, resting state fMRI, 133 direction multi shell DWI, and 2 fieldmaps for the functional data (one reversed phase encoding direction, one Siemens deafult fieldmap sequnce) and one fieldmap for the DWI (reversed field encoding direction). An additional reference image of the resting state fMRI is included without multiband factor.
ToDo:
Questionnaires data are also acquired and can be found in the ... fodler.

The proposal can be found here: ToDo link

The BIDS conversion was done with heudiconv by the Z03 project coordinators.

Defacing
--------------------------------------------------------------------
Defacing was done by the Z03 cooridnator.
Pydeface was used on all anatomical images to ensure deindentification of subjects. The code
can be found at https://github.com/poldracklab/pydeface


Known Issues
--------------------------------------------------------------------
N/A 

--------------------------------------------------------------------

