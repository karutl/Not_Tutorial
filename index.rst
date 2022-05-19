Main Page
____________________________
___________________________
NANOME is a tool used to extract information from the Pipeline. It is often used by scientists to gain a better understanding of various illnesses, such as cancer, 
by extracting specific information from the pipeline. 


NANOME is used with various documentation tools, such as Nextflow. There are various applications that you will need to download, including nextflow.


In this tutorial, we will be looking at how to get started with nanome, including installing programs such as nextflow!



If you are using a mac, you will need to install Anaconda[(https://www.anaconda.com/)] to do the following in this tutorial. If you are on a windows, please install 
PUTTY [(https://www.putty.org/)] or MobaX [(https://mobaxterm.mobatek.net/download-home-edition.html]) as well as Anaconda


Installation
_____________________
_____________________


On a mac:

Please type the following in your anaconda terminal:

conda install -c conda-forge -c bioconda nextflow

On a windows:

Please use the PUTTY or MobaX terminal that you downloaded and type this command:

wget -qO- https://get.nextflow.io | bash



On windows, the command typed above on anaconda might not always work with windows! Therefore, installation on hpc might be required.
This command is used to download nextflow on the hpc! 

Quickstart - ecoli
_______________________
_______________________

In your terminal, please download this ecoli dataset:

wget http://s3.climb.ac.uk/nanopolish_tutorial/ecoli_2kb_region.tar.gz
tar -xvf ecoli_2kb_region.tar.gz
cd ecoli_2kb_region

Quickstart - human
_________________________
__________________________

Quickstart - cloud computing platform
____________________________________
___________________________________

Quickstart - QC Analysis
_______________________________
_______________________________

Help us Debug NANOME
______________________________
______________________________

Manual
_______________________
______________________

Sources
____________________
____________________

Yang Liu "NANOME Pipeline (Nanopore long-read Sequencing Data Consensus DNA Methylation Detection) Github ([https://github.com/LabShengLi/nanome])

"Get Started" Nextflow

MobaXTerm

PuTTY

Anaconda

"Quickstart - How to Polish a Genome Assembly" Nanopolish
