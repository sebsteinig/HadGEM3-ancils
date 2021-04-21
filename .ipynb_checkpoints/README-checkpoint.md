# HadGEM3-ancils

Collection of interactive jupyter notebooks to reproduce and document the ancillary files for my HadGEM3 experiments. Notebooks are written in python 3.7.
Each directory is self-contained and includes all files and notebooks necessary to create the non-default ancillaries for one single experiment stated in the directory name. 

## Running the notebooks
Individual notebooks need to be run in the given order as some processing might depend on changes to the land-sea mask or ice cover. Notebooks can be accessed and run by the Binder link above for convenience, but please note that this will not allow to modify or create files on disk. To create new ancillary files for production 

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/sebsteinig/HadGEM3-ancils/HEAD)
