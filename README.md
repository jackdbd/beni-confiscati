# Beni Confiscati

[![Binder](https://mybinder.org/badge.svg)](https://mybinder.org/v2/gh/jackdbd/beni-confiscati/master)

Exploratory data analysis and visualization of a small geospatial dataset.

Explore the [interactive map](https://jackdbd.github.io/beni-confiscati/).

![An image showing a map of Tuscany created with Folium](https://raw.githubusercontent.com/jackdbd/beni-confiscati/master/screenshots/folium-map.png "The map created with Folium.")

Built with:

- Geopandas
- Shapely
- PyProj
- Cartopy
- Folium


## Data

Source: Regione Toscana – [Beni confiscati alla criminalità organizzata](http://dati.toscana.it/dataset/rt-beniconfiscati) (January 2018).

The dataset is released under the [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) license.


## Run the notebook with Binder
[Binder](https://github.com/jupyterhub/binderhub) builds a docker image from a git repository + commit, so you can run the notebook `beni-confiscati.ipynb` in the cloud, without installing anything on your machine.


## Installation

If you want to run the notebook locally, you need to create a conda environment. You can obtain the conda package manager by installing a Python distribution like [Miniconda](https://conda.io/miniconda.html) or [Anaconda](https://repo.continuum.io/).

Create and activate a new conda environment:

```shell
conda create --name beni-confiscati python=3.6 --yes
source activate beni-confiscati
```

Install all the dependencies (this might take a while, go grab a cup of coffee):

```shell
conda install -c conda-forge jupyter numpy pandas geopandas pyproj shapely cartopy folium -y
```

If you run into issues when importing `fiona`, try downgrading it to `1.7.9`:

```shell
conda install -c conda-forge fiona=1.7.9
```

When all dependencies have been installed, run the notebook:

```shell
jupyter notebook
```

*Note:* I decided to included the dataset in the repository, so you don't have to go find it by yourself. After all it is just ~200KB.


## Other

You can freeze your environment with:

```shell
conda env export > environment.yml
```

To remove this conda environment, run:

```shell
conda env remove -n beni-confiscati
```
