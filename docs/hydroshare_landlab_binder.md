# Software Instructions to Access an Interactive Notebook 
## This resource provides a Landlab Developer Software Environment that is enables data transfer from a HydroShare Resource using the Binder platform. 

### Instructions for Quick Access, Updating Data and Updating Code

# Quick access to run code online

To open interactive Jupyter Notebooks with Binder JupyterHub server. You will be connected to a virtual machine with the software environment required to execute the models.

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/hydroshare/https%3A%2F%2Fwww.hydroshare.org%2Fresource%2F4cac25933f6448409cab97b293129b4f/)

When your personal compute workspace is finished building (thank you Binder), you will see a file directory (thank you JupyterHub). 
Click on the Amazing_Landlab_ModelInstance.ipynb Notebook (thank you Landlab).  This notebook is also viewable but not interactive in it's development location (thank you Github). 


## Online Modeling Instructions 

To open interactive Jupyter Notebooks with the CUAHSI JupyterHub server, go to the upper right corner of the resource page and click on 'Open With'. Select CUAHSI JupyterHub.  You will be connected to a virtual machine with the software environment required to execute the models.

Notebook 1: Learn about Landlab functions with a synthetic grid and recharge forcings

Notebook 2: Learn about Version 2 Landslide Component comparing depth to water table and recharge forcings on a synthetic grid

Notebook 3: Replicate an experiment on a watershed subset within regional Landlab landslide model to explore fire impacts. The resource was originally derived from a reproducible demonstration of the landslide modeling results from: Strauch, R., Istanbulluoglu, E., Nudurupati, S. S., Bandaragoda, C., Gasparini, N. M., and Tucker, G. E.: (2018) A hydro-climatological approach to predicting regional landslide probability using Landlab, Earth Surf. Dynam. Discuss., https://doi.org/10.5194/esurf-6-49-2018:  Replicate_landslide_model_for_fire.ipynb

## Create a Software Environment for a Github Repository - Personal Computer Installation Instructions 

### Packages

The notebooks included in this resource require the following Python 3 packages:

```
hs_restclient==1.3.5
landlab==1.10.0  

```

To ensure that you have the correct packages and versions, run the following command(s) inside a Python terminal:

```
$ conda list
```

or 

```
$ pip list
```

### Creating a Landlab Working Environment on Binder from HydroShare

We recommend using Anaconda to create a fresh Python environment with all dependencies installed. After installing Anaconda, simply run the commands below with your desired environment name in place of `MY_ENVIRONMENT_NAME`:

Landlab Installation of latest release: See [Installing Landlab](https://landlab.readthedocs.io/en/master/install/)

Landlab Installation of your development branch: See [Installing Landlab for Development](https://landlab.readthedocs.io/en/stable/dev_guide_install.html)

```
conda create -n MY_ENVIRONMENT_NAME --file requirements.txt
```

activate the environment and start a jupyter server

```
source activate MY_ENVIRONMENT_NAME
jupyter notebook
```
### Debugging a Working Environment
Are you getting errors?  Here are some suggested steps. If you still have issues, email help@cuahsi.org or reach out to us (comment on this resource or see emails in HydroShare profiles) and we will invite you to the HydroShare Slack #landlab channel. 

Bug: PackagesNotFound

```
PackagesNotFoundError: The following packages are not available from current channels.
```

Reduce the number of packages that were not available by running the following command

```
conda config --append channels conda-forge
```

Bug: Conda vs.Pip Install

If you get errors for a few packages, remove them from the requirements.txt file until you successfully created the conda environment.

```
conda create -n MY_ENVIRONMENT_NAME --file requirements.txt
```

Any packages that didn't get installed during creation of conda environment can be pip installed separately in the newly created conda environment.
for example: 

```
pip install hs-restclient==1.3.5
```

### Reproducible Quote of the Day:

"The product of mental labor - science - always stands far below its value, because the labor-time necessary to reproduce it has no relation at all to the labor-time required for its original production."  Karl Marx


