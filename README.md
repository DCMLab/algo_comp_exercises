# Algorithmic Composition

## Setting up the environment for the exercises

Throughout the course, we will be using the interactive Python interpreter `IPython` through the famous Jupyter interface.

### Anaconda

Anaconda provides the easiest entry point for Python newcomers and for us the easiest way to make sure our notebooks run on everyone's system. 

* If you don't have it installed already, please [install Anaconda](https://docs.anaconda.com/anaconda/install/). The installer is >500 MB so make sure you install it with a good and unlimited internet connection.
* If you do, please bring conda up to date: `conda update -n base -c defaults conda`

> Unless you know what you're doing, use the `(Anaconda) Command Prompt` for all shell commands.

### MuseScore

If you were learning about a single Python library in this course, it would be `music21`. For it to display music notation, it requires you to install the open-source notation software [MuseScore 3](https://musescore.org/download). For configuring `music21` (see below) you will need to know the location of your MuseScore executable.

### Create the `algo` environment

1. Clone this repository
  * using the Git software: `git clone https://github.com/DCMLab/algo_comp_exercises.git` (if you have never used it, you might have to [install it](https://git-scm.com/downloads) first
  * beginners: you can download the files in the form of [this ZIP file](https://github.com/DCMLab/algo_comp_exercises/archive/main.zip). 
3. Navigate to your clone using `cd [FOLDERNAME]`
4. Create a new environment `algo` with all dependencies installed: `conda env create -f 01/algo_env.yml` (on Windows paths use backslashes: `conda env create -f 01\algo_env.yml`)
5. Activate the new environment: `conda activate algo`
6. Start JupyterLab: `jupyter lab` (it is a more convenient alternative to `jupyter notebook` which would work as well)
7. Navigate to the folder `01` and open the notebook `01_introduction.ipynb`.
8. Execute the first cell (the one with a lot of `import` statements) to see whether you get any errors. If you do, you probably need to click to open the menu on the top right (which should say something with 'Python') end select your `algo` environment. Then, try again.
    * `Ctrl/Cmd + Enter` to execute a cell
    * `Shift + Enter` to execute a cell and go to the next one

## Configure `music21`

To display notated music, the library `music21` calls `MuseScore` to obtain an PNG image. Therefore, we need to tell it where to find MuseScore on your computer. In the corresponding cell of the notebook, the most likely path for every type of OS (Linux, Windows, Mac) is given. Make sure to uncomment (remove `#`) the line for your system and to comment out (leading `#`) the other two before running the cell.
