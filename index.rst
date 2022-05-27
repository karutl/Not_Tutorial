Main Page
____________________________
___________________________
NANOME is a tool used to extract information from the Pipeline. It is often used by scientists to gain a better understanding of various illnesses, such as cancer, 
by extracting specific information from the pipeline. 


NANOME is used with various documentation tools, such as Nextflow. There are various applications that you will need to download, including nextflow.


In this tutorial, we will be looking at how to get started with nanome, including installing programs such as nextflow!



If you are using a mac, you will need to install Anaconda (https://www.anaconda.com/) to do the following in this tutorial. If you are on a windows, please install 
PUTTY (https://www.putty.org/) or MobaX (https://mobaxterm.mobatek.net/download-home-edition.html) as well as Anaconda


Installation
_____________________
_____________________


On a mac:

Please type the following in your anaconda terminal:

``conda install -c conda-forge -c bioconda nextflow``

On a windows:

Please use the PUTTY or MobaX terminal that you downloaded and type this command:

``wget -qO- https://get.nextflow.io | bash``



On windows, the "conda" command might not always work! Therefore, installation on hpc might be required.
This command is used to download nextflow on the hpc! 

E.coli
_______________________
_______________________

In this section, you will be using your terminal to download and analyze ecoli data. You can analyze this dataset in conda, hpc, or other terminals. 

The command for running e.coli data is the same as the command for running human data. This is the command:

``nextflow run LabShengLi/nanome.``
Please note that the ``--genome`` part of the command is set as human as a default. In order to change this, please set the ``--genome`` as e.coli. After you do this, please type the following:

``nextflow run LabShengLi/nanome\``
    ``-profile singularity,hpc \``
    ``-config  conf/examples/ecoli_demo.config``



Human
_________________________
__________________________

In this section, we will be analyzing human data trough the terminals. Please enter the following command in your Anaconda prompt, PUTTY prompt, or MobaX Prompt:

Please type the following command below

``nextflow run LabShengLi/nanome.``

If you need assistance with running this command, then please type the following in your terminal:

``nextflow run LabShengLi/nanome --help``


Cloud Computing Platform
____________________________________
___________________________________

In this section, we will be analyzing the Cloud Computing Platform for analyzing datasets.

There are various cloud computing platforms. One of them is Google Cloud Platform.

Here, we will be taking a look at how to analyze data trough Google Cloud Platform.

To start, please download the google API by accessing this link (https://anaconda.org/conda-forge/google-cloud-sdk) and type the following code in your anaconda terminal below: 

``conda install -c conda-forge google-cloud-sdk``

Then, authennticate by typing:

``gcloud auth login --no-launch-browser``
``gcloud auth application-default login``

Next, make sure to name your project to the config file ~/.config/gcloud/application_default_credentials.json.
``"project_id": "[PROJECT-ID]",``

After that, please set the project by typing the following:

``gcloud config set project [PROJECT_ID]``

Next, please make sure to export the enviornmental variables. The variables can be put in ~/.bashrc

``export NXF_VER="20.10.0"``
``export NXF_MODE=google``
``export NXF_DEBUG=3``
``export PROJECT="[PROJECT_ID]"``
``export GOOGLE_APPLICATION_CREDENTIALS=~/.config/gcloud/application_default_credentials.json``

Once you are done exporting the envionrment variables, you can run the Google Cloud Platform on nextflow.

``nextflow run LabShengLi/nanome\``
     ``-profile test,docker,google\ ``
     ``-w [Google-storage-bucket]/nanome-work-test\``
     ``--outdir [Google-storage-bucket]/nanome-outputs\``
    `` --googleProjectName  [PROJECT_ID]``
    
QC Analysis
_______________________________
_______________________________

QC Analysis stands for "Quality Control Analysis." This assesses the quality of nanome. There are various datasets that you can use to assess the quality of each dataset. You can choose any dataset. 


Sources
____________________
____________________

Yang Liu "NANOME Pipeline (Nanopore long-read Sequencing Data Consensus DNA Methylation Detection) Github ([https://github.com/LabShengLi/nanome])

"Get Started" Nextflow

MobaXTerm

PuTTY

Anaconda

"Quickstart - How to Polish a Genome Assembly" Nanopolish

Yang Liu "Running Pipeline on Google Cloud Platform" https://github.com/LabShengLi/nanome/blob/master/docs/CloudComputing.md

