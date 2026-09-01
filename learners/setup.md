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
### Install uv

`uv` is a Python package manager and environment tool. Use the 
[uv installation guide](https://docs.astral.sh/uv/getting-started/installation) 
to install `uv` if it is not already installed.

### Ensure no environment is active before you start

If any environment auto‑activates when you open PowerShell (Windows) or
a terminal (MacOS / Linux), deactivate it. Otherwise `uv` may not behave 
correctly.

See the official documentation of your package manager (e.g. conda) 
for details.

For conda, the relevant section is 
[Deactivating an environment](https://docs.conda.io/projects/conda/en/4.6.1/user-guide/tasks/manage-environments.html#deactivating-an-environment)


### Create an environment with the required Python packages

::::::::::::::::::::: spoiler

#### Windows
Run the commands below in PowerShell.
Lines starting with # are comments and will not be run.
    
``` bash
# Create a project folder (e.g. napari-ai-workshop) and move into it
mkdir napari-ai-workshop
cd napari-ai-workshop
# Update uv
uv self update
# Create a virtual environment 
uv venv
# Activate the environment
.venv\Scripts\activate
# Install required Python packages
uv pip install micro-sam napari-matplotlib napari-skimage-regionprops jupyterlab ipywidgets git+https://github.com/ChaoningZhang/MobileSAM.git
```
:::::::::::::::::::::

::::::::::::::::::::: spoiler

#### MacOS
Run the commands below in the terminal. Lines starting with `#` are comments that will not be run.

You can run the commands by copy pasting them into the terminal and pressing the Enter key.

    
``` bash
# Create a project folder (e.g. napari-ai-workshop) and move into it
mkdir napari-ai-workshop
cd napari-ai-workshop
# Update uv
uv self update
# Create a virtual environment 
uv venv
# Activate the environment
source .venv/bin/activate
# Install required Python packages
uv pip install micro-sam napari-matplotlib napari-skimage-regionprops jupyterlab ipywidgets git+https://github.com/ChaoningZhang/MobileSAM.git
```
:::::::::::::::::::::

::::::::::::::::::::: spoiler

#### Linux
Run the commands below in the terminal.
Lines starting with # are comments and will not be executed.

``` bash
# Create a project folder (e.g. napari-ai-workshop) and move into it
mkdir napari-ai-workshop
cd napari-ai-workshop
# Update uv
uv self update
# Create a virtual environment
uv venv 
# Activate the environment
source .venv/bin/activate
# Install required Python packages
uv pip install micro-sam napari-matplotlib napari-skimage-regionprops jupyterlab ipywidgets git+https://github.com/ChaoningZhang/MobileSAM.git
```
:::::::::::::::::::::


### Testing the installation
After installing the packages and activating your `napari-ai-workshop` environment, you should be able to launch napari and JupyterLab.

To test whether napari opens, run:
``` bash
napari
```
An empty image viewer window titled `napari` should appear. This can take a few moments, especially the first time.
    
To check that JupyterLab launches correctly, run:
``` bash
jupyter lab
```
    
Your default web browser should open JupyterLab. It may open in a new tab or a new window, depending on your browser settings.


::::::::::::::::::::::: spoiler
## Further Napari exploration

We are providing an optional environment for people who want to explore 
other napari plugins outside of this workshop. You do **not** need to create
this environment for the workshop, and none of the course materials or website 
use this environment.

The reason: installing `micro_sam` plugin may disable the ability to search 
for plugins using the napari GUI. So if you want to explore other plugins, 
it is be best to do so in a separate environment without `micro_sam`.

To create a seperate environment, navigate outside of the 
`napari-ai-workshop` folder. You can do this by moving up one directory.
``` bash
cd ..
```
Next, follow the instructions below.
If you do not already have conda installed 
(e.g. via Miniforge, Anaconda or similar), download and install the latest 
[Miniforge distribution](https://conda-forge.org/download/) for your 
operating system. 

::::::::::::::::::::::: tab
### Windows

Run the commands below in PowerShell.
Lines starting with # are comments and will not be run.
    
``` bash
# Create a project folder (e.g. napari-workshop) and move into it
mkdir napari-env
cd napari-env
# Update uv
uv self update
# Create a virtual environment
uv venv 
# Activate the environment
.venv\Scripts\activate
# Install napari and JupyterLab
uv pip install "napari[all]" jupyterlab ipywidgets
```
    
### MacOS
    
Run the commands below in the terminal. Lines starting with `#` are comments that will not be run.

You can run the commands by copy pasting them into the terminal and pressing the Enter key.

    
``` bash
# Create a project folder (e.g. napari-workshop) and move into it
mkdir napari-workshop
cd napari
# Update uv
uv self update
# Create a virtual environment 
uv venv
# Activate the environment
source .venv/bin/activate
# Install napari and JupyterLab
uv pip install "napari[all]" jupyterlab ipywidgets
```
    
### Linux

Run the commands below in the terminal.
Lines starting with # are comments and will not be executed.

``` bash
# Create a project folder (e.g. napari-workshop) and move into it
mkdir napari-workshop
cd napari-workshop
# Update uv
uv self update
# Create a virtual environment called "napari-env"
uv venv 
# Activate the environment
source .venv/bin/activate
# Install napari and JupyterLab
uv pip install "napari[all]" jupyterlab ipywidgets

```
    
:::::::::::::::::::::::::
:::::::::::::::::::::::::



