# Generate HadGEM3 ancillary files

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/sebsteinig/HadGEM3-ancils/HEAD)

Collection of interactive jupyter notebooks to reproduce and document the ancillary file 
generation for my HadGEM3 experiments. Notebooks are written in python 3.7. Each directory 
is self-contained and includes all files and notebooks necessary to create the non-default 
ancillaries for the single experiment stated in the directory name. Individual notebooks 
should be run in the given order as some processing might depend on changes to the land-
sea mask or ice cover in a previous step.

## Running the notebooks
Notebooks can be accessed and run by the Binder link above for convenience, but note that 
this will not allow to modify or create files on disk. To create new ancillary files for 
production download the respective directory for the experiment and run the notebooks 
locally. Easiest way is to install [conda](https://conda.io/projects/conda/en/latest/index.html) 
and create an environment `env_name` with 

```
conda env create --name env_name --file=environment.yml
``` 

using the `environment.yml` file from this repository. The notebooks can then be run 
interactively by typing

```
jupyter notebook
```

or directly from the command line with

```
jupyter nbconvert --to notebook --inplace --execute notebook_name.ipynb
```

## Converting to Unified Model (UM) format
Notebooks produce initial and boundary condition files in netCDF format for easier
manipulation and plotting. HadGEM3 expects those to be in UM format. 
[Xancil](http://cms.ncas.ac.uk/documents/xancil/) is installed on 
[NEXCS](http://cms.ncas.ac.uk/wiki/NEXCS) and can be used to convert the newly created 
netCDF files to UM format. Run xazncil on NEXCS via

```
~jecole/bin/xancil
```


Need to add description on how to run xancil on command line and document some quirks for
individual ancils.
