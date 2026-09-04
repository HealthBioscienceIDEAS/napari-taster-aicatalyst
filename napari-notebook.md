---
title: 'Using Napari through Jupyter'
teaching: 10
exercises: 0
---

:::::::::::::::::::::::::::::::::::::: questions 

- How can you interact with Napari in a notebook?
- How are images represented in the computer?
- What are the main structures that Napari uses to represent imaging data?
- How can we get basic measurements out from this

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives
- Understand how to open and interact with Napari via JupyterLab notebooks

::::::::::::::::::::::::::::::::::::::::::::::::

Instead of entering Python commands in Napari’s built‑in console, 
we will write and run our code in a [computational notebook](https://docs.jupyter.org/en/latest/#what-is-a-notebook) 
using [JupyterLab](https://jupyterlab.readthedocs.io/en/stable/index.html). 
This allows us to build a reusable workflow that is easy to repeat and adapt.

We have kept the level of programming knowledge required to the minimum
possible and all code can be run by copy and pasting, so don't worry if
you don't understand it all yet.

Most, if not all, of the functions we will use in this lesson are also
accessible via various Napari plugins, so the analysis pipeline could also be
assembled within Napari if you prefer.

## Creating a notebook in JupyterLab

### 1. Activate your Napari environment
Open the terminal (the same one you used for Napari installation: 
see 'Opening a terminal' section of [the setup instructions](https://healthbioscienceideas.github.io/microscopy-novice/index.html)), 
and activate the environment you created for Napari:
``` bash
cd napari-ai-workshop
source .venv/bin/activate
```

### 2. Launch JupyterLab
Start JupyterLab:
``` bash
jupyter lab
```
The JupyterLab interface should appear in a browser window.

### 3. Create and navigate to your workshop folder
It is best practice to keep all your project files together in a dedicated folder.

- Use the file browser on the left-hand side
- Navigate to a location that is easy to find again (like your Desktop)
- Right-click to create a new folder and name it *workshop-notebooks* 

### 4. Create a new notebook
Once you are inside the *workshop-notebooks* folder, create a new notebook.

For example by using the JupyterLab menu bar to select: **File > New > Notebook > Python 3 (ipykernel)**

This will open a new Python notebook.

### 5. Name your notebook
Renaming your notebook immediately helps keep your workflow tidy and makes it easier to find later.

Right click the default name at the top of the notebook tab (e.g., *Untitled.ipynb*), and select `Rename Notebook...`.

Enter a meaningful name, for example: *image_display.ipynb*.

## About notebooks

::::::::::::::::::::::: instructor
### Say you assume people have worked with Jupyter notebooks before 
But if not, we will provide more of a primer in the materials at the end
of the workshop.
:::::::::::::::::::::::

A notebook is made up of building blocks called **cells**.

For this workshop, we will only use **Code Cells**. 

When you run a Code Cell, the output typically appears underneath it. This could be a number, text, a table, or an error message.

By splitting code up into cells, you can run one specific part of your code without having to re-run the whole file and get instant feedback.

Be careful about the order of your notebook cells. Running them out of sequence can leave variables outdated or missing, which can lead to confusing results. 

## Using Python inside a notebook

Run each of the following examples in separate notebook cells so you can clearly see the output after each step.

``` python
# Everything after a hash (#) is a comment and is ignored by Python.
# Use comments to explain what you're doing.
```

If you want to create another cell, click the **+** button in the toolbar or use the **Insert Cell Below** button on the right side of the cell.

``` python
# Python can do basic calculations
1 + 1
1 + 2
# and will display the last output
```

``` output
3
```

``` python
# Python can assign values to variables
one = 1
two = one + one
```

Notice that there is no output.

``` python
# Variables store values rather than return them
# To see their value write the variable name
two
```

``` output
2
```

**Note**: In a standard Python script, writing a variable name on its own does nothing and you must use `print()` to show output.


``` python
# Python's print function
print("one plus one is", two)
print("one plus two is", one + two)
```

``` output
one plus one is 2
one plus two is 3
```

## Using Napari from within a notebook

First import napari
``` python
# Import napari package
import napari
``` 

Then open it from the notebook
``` python
# Open Napari from the notebook
viewer = napari.Viewer()
```

Finally open a sample image. 
``` python
# Open Cells (3D + 2Ch) sample image in napari's viewer
viewer.open_sample("napari", "cells3d")
```

The output should look like this:

``` output
[<Image layer 'membrane' at 0x1853b7738c0>,
 <Image layer 'nuclei' at 0x1853c844710>]
 ```

The memory addresses (`0x1853b7738c0` and `0x1853c844710`) will be different for you. They indicate the locations in memory where Python happened to store those layer objects. 

Napari's viewer should open in a separate window, preloaded with the cells3D sample image.

Now that we are able to interact with Napari via a lab-book, let's 
now look more into the structure of imaging data. 


::::::::::::::::::::::::::::::::::::: keypoints 

- You can interact with Napari both through the interface, it's built-in
console or through a Jupyter lab notebook
- Napari represents all elements for viewing (Images, Points, etc) as layers

::::::::::::::::::::::::::::::::::::::::::::::::

