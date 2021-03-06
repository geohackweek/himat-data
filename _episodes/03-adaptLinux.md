---

title: "NASA ADAPT: Linux VM"
teaching: 10
exercises: 0
questions:
- "How do I initiate a Linux VM session on ADAPT?"
- "Where can I find various HiMAT datasets?"
- "What storage resources do I have access to?"
objectives:
- "Learn the necessary steps to initiate a Linux VM on ADAPT"
- "Become familiar with navigating the Linux ADAPT command line environment"
- "Learn what kinds of software and processing we can carry out on the Linux VM"
keypoints:
- "The Linux VM provides us with maximum flexibility in accessing and manipulating HiMAT datasets (relative to the Windows VM)"

---

## Start the Linux VM

You should be at a command prompt within ADAPT (last lesson). Next, SSH to one of the 15 himat VMs:

~~~
[aarendt@ngalogin02 ~] $ ssh himat101
~~~
{: .bash}

Here we chose the himat101 VM, and we're assuming we already connected as userID = aarendt. You can use any of the himat102, himat103,...himat115 VMs.

After this your terminal prompt will look like:

~~~
aarendt@himat101:~$
~~~
{: .bash}

## ADAPT Datasets

ADAPT provides HiMAT with direct access to the full Landsat, MODIS and MERRA [data sets](https://www.nccs.nasa.gov/services/adapt/data). You can view these datasets by typing:

~~~
aarendt@himat101:~$ ls /att/pubrepo
~~~
{: .bash}

You'll see this list of folders:

~~~
ABoVE_products  LANDSAT  misc_products  NGA             obsolete
DEM             MERRA    MODIS          NGA_footprints
hma_data        MERRA2   new_NGA        NGA_Incoming
~~~
{: .bash}


As team members generate new products, we will be hosting these in a file structure similar to that used for the existing NASA remote sensing and climate reanalysis datasets. 


Each user also has access to a 15 GB home directory, in my case:

~~~
/home/aarendt
~~~
{: .bash}

and a 5 TB nobackup/scratch directory for large temporary files.

~~~
/att/nobackup/aarendt
~~~
{: .bash}

HiMAT will track the location of all files on a [secured website](http://himat.org/team-documents/data-access/) accessible to the team. 

## Customizing your ADAPT environment

Each ADAPT user is assigned space on a \home directory. Within this directory you can install your own custom software provided it is available via open-source. For example, we have successfully installed [anaconda](https://geohackweek.github.io/Introductory/00-conda-tutorial/) in our home directory enabling us to build custom Python environments. 

### Python

Note that NCCS has enabled pip install capabilities for us on all HiMAT VMs. 

### Matlab

Information here on how to install a Matlab license.

## Graphical User Interfaces to ADAPT

Several software packages on ADAPT can be accessed in a GUI/Windows-type interface. Within any Linux VM you can run QGIS from the command line, and this will create another terminal window in which you can use QGIS software. The advantage in doing so is that you can browse satellite imagery (e.g. the High Resolution DEM products) without having to download them to your local machine. Note that in some cases there are time delays that might limit effectiveness of this approach, but NCCS is working on solutions.

