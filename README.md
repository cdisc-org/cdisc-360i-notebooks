<p align="center">
    <a href="www.cdisc.org">
        <img src="images/CDISC-360i-Logo.png" alt="CDISC 360i" width="200" height="200">
    </a>
</p>

---

<p align="center">
    <a href="https://colab.research.google.com/">
        <img src="images/icons8-google-colab-48.png" alt="Google Colab" />
    </a>
</p>


[![Python 3.12](https://img.shields.io/badge/python-3.12-blue.svg)](https://www.python.org/downloads/release/python-3120)

# Abstract #

CDISC 360i defines a vision and roadmap to enable standards-driven automation across the clinical research data life cycle - from study design to analysis. The purpose of these notebooks is to demonstrate the 360i Technical Roadmap by showcasing a strategy for research data pipeline automation using end-to-end, machine-readable standards metadata.

These notebooks automate study design using concepts and a standardized model to build a digital protocol. Aligned Case Report Forms (CRFs) and SDTM resources will be automatically generated as downstream artifacts using metadata from the digital protocol.


# Notebooks #

## Google Colab Notebooks
Currently, these notebooks are designed to execute in the [Google Colaboratory](https://colab.google.com/) environment.

|Notebook                                   |Notes
|-------------------------------------------|-------------------------------------------------------------------|
|CDISC_360i_Object_Store_Automation         |* Does not copy study artifacts to filesystem, but works entirely with objects in Object Store    |
|                                           |* Uses Google Drive as Object Store                                |
|                                           |* Requires Colab env setup for Google Drive                        |
|                                           |* Development will continue as new tools and features become available |
|CDISC_360i_Protocol_to_Submission          |* Shown at CDISC Interchange                                       |
|                                           |* Copies study artifacts to local filesystem prior to copying to Object Store  |
|                                           |* Uses Google Drive as Object Store                                |
|                                           |* Requires Colab env setup for Google Drive                        |
|                                           |* Development has stopped for this version                         |

### How To ###

#### CDISC_360i_Protocol_to_Submission Notebook ####

1. Clone the repository or download notebook and resources.
2. Access [Google Colaboratory](https://colab.google.com/) using your Google account.
3. Setup MyDrive to match URL requirements of notebook.  The directory structure in Google Drive should appear as:


    ![MyDrive/resources/ directory structure](images/resources.png)

    This will ensure the code cells in the CDISC_360i_Protocol_to_Submission notebook execute correctly.

4. Copy the CDISC_360i_Protocol_to_Submission notebook to the myDrive/Colab Notebooks directory:

    ![MyDrive/Colab Notebooks directory structure](images/ColabNotebooks.png)

5. A custom distribution of the CDISC CORE Rules Engine will be required for execution of CORE Validation Rules in the notebooks.  This distribution will need to be built for the system hosting the notebooks.  Instructions are available here:

    https://github.com/cdisc-org/cdisc-rules-engine/blob/main/README_Build_Executable.md

    The custom distribution used in the notebooks is too large for GitHub.

    Ensure the new distribution is renamed as core.tar.gz and stored as shown in the image above.


**Notes:**
* The notebook relies upon access to your Google Drive.
* If you would like to access the OpenStudyBuilder API, you must supply a BEARER_TOKEN.
* The *core.tar.gz* used in the notebook is a distribution of the CORE engine built for the Google Colab environment as of October 2025.  Google Colab environment future updates may require the creation of a new distribution of the CORE engine (links are included in the notebook).

#### CDISC_360i_Object_Store_Automation ####

1. Clone the repository or download notebook and resources.
2. Access [Google Colaboratory](https://colab.google.com/) using your Google account.
3. Copy notebook into Google Colab environment.
4. Follow instructions in the Notebook.

**Notes:**
* Once the directories are created in *Google MyDrive*, copy the *Definte-Template.json* file and the *input_files* directory into the */content/drive/MyDrive/TMF* dirctory.


# Resources #
**Other GitHub projects used in the notebooks**

|Project                            |GitHub Repository                                                                          |
|-----------------------------------|-------------------------------------------------------------------------------------------|
|Study Definition Workbench         |https://github.com/data4knowledge/study_definitions_workbench                              |
|Open Study Builder                 |https://gitlab.com/Novo-Nordisk/nn-public/openstudybuilder/OpenStudyBuilder-Solution       |
|Study USDM documents               |https://github.com/cdisc-org/360i/tree/main/data/protocol/LZZT/usdm                        |
|USDM validation utility            |https://github.com/pendingintent/cdisc-json-validation                                     |
|CDISC CORE Rules Engine            |https://github.com/cdisc-org/cdisc-rules-engine                                            |
|CRF creation                       |https://github.com/lexjansen/cdisc360i-pocs                                                |
|Trial Design Dataset creation      |https://github.com/pendingintent/cdisc-usdm-utils                                          |
|Define-XML template creation       |https://github.com/dostiep/360i                                                            |
|Define-XML creation                |https://github.com/swhume/template2define                                                  |
|Raw subject data                   |https://github.com/alidootson/UpdatedCDISCPilotData/tree/main/UpdatedCDISCPilotData/CDASH  |