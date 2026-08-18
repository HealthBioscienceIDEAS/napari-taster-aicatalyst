---
title: Setup
---

FIXME: Setup instructions live in this document. Please specify the tools and
the data sets the Learner needs to have installed.

## Data Sets
No datasets will be required to download for this taster session.
All images will be pre-loaded examples that are already part of Napari. 
Provided Napari software is loaded correctly, you are all set!

## Software Setup
### Install conda

If you do not already have conda installed 
(e.g. via Miniforge, Anaconda or similar), download and install the latest 
[Miniforge distribution](https://conda-forge.org/download/) for your 
operating system. 

### Use conda from terminal

Follow the instructions below to open a terminal on your operating system.

:::::::::::::::: spoiler

#### Windows (Miniforge)

- Click Start
- Search for **Miniforge Prompt**
- Click to open

:::::::::::::::::::::::::

:::::::::::::::: spoiler

#### Windows (Anaconda)

- Click Start
- Search for **Anaconda Prompt**
- Click to open

:::::::::::::::::::::::::

:::::::::::::::: spoiler

#### MacOS

- Open **Launchpad**
- Go to **Other**
- Open **Terminal**

:::::::::::::::::::::::::


:::::::::::::::: spoiler

#### Linux

- Open any terminal window

:::::::::::::::::::::::::


### Install python packages
Once you have gone into conda, we are going to create an environment specific
to this spoiler and then install the packages needed for the workshop.

:::::::::::::::: spoiler
#### MacOS
    
Run the commands below in the terminal. Lines starting with `#` are comments that will not be run.

You can run the commands by copy pasting them into the terminal and pressing the Enter key.
    
``` bash
# Update conda
conda update -n base conda
# Create a virtual environment called "napari-env" and install napari
conda create -y -n napari-env -c conda-forge python=3.12 napari pyqt
# Activate the environment
# This should change the terminal prompt to '(napari-env)'
conda activate napari-env
# Install JupyterLab and dependencies 
pip install --upgrade jupyterlab ipywidgets  
```
    
:::::::::::::::::::::::::

:::::::::::::::: spoiler
#### Other operating systems including Windows
        
Run the commands below in the terminal. 
Lines starting with `#` are comments that will not be run.

You can run the commands by copy pasting them into the terminal and pressing the Enter key.
    
``` bash
# Update conda
conda update -n base conda   
# Create a virtual environment called "napari-env"
conda create -y -n napari-env -c conda-forge python=3.12   
# Activate the environment
# This should change the terminal prompt to '(napari-env)'
conda activate napari-env
# Install napari and plugins using pip
pip install "napari[all]" napari-bioio-reader bioio-czi
# Install JupyterLab and dependencies 
pip install --upgrade jupyterlab ipywidgets 
```
    
:::::::::::::::::::::::::



