# Data Science 

<p align="center">
  <img src="https://github.com/ridasilva/bioestatistica/blob/master/img/logo.png" alt="logo"/>
</p>

## Installation

Install conda

```
wget https://repo.continuum.io/miniconda/Miniconda2-latest-Linux-x86_64.sh
bash Miniconda2-latest-Linux-x86_64.sh

```
   
Create a dedicated conda environment and activate

```
conda env create -f environment.yml
conda activate datascience 
```

If a new library needs to be installed, don't forget to update the environment.yml file 

```
conda env export | grep -v "^prefix: " > environment.yml 
```

### Building jupyter-book

Before building, use the edit cell codes to hide with

```
python edit_notebooks.py YOUR_NOTEBOOK
```

Build

```
jupyter-book build DataScience/
```

You can preview the result on `_build/html/index.html`.

After the build, publish the notebook.

```
ghp-import -n -p -f _build/html
```

