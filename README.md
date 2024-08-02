## GY485 Dissertation: Food Desert Specification

This repository contains the coding files employed to conduct the data analysis for the 2023-2024 MSc Geographic Data Science Dissertation (GY485). The coding script in this repository depends on open source packages and a python module written the same author for collecting ONS census 2021 data ([cwtravisyip/ONS_Census2021](https://github.com/cwtravisyip/ONS_Census2021)). In addition to the script stored in this repository, a python file `api_key.py` is also required to successfully request data from the ONS Beta API and the visualisation dependant on Stadia. This python file should include the following variables:
* stadia_key
* user_agent_ons
* nasa_earthdata_token

The jupyter notebook and the R markdown files are named in accordance to their row in the data pipeline, where the two-digit preffixes denote the sequential order or the data processes.

The data used in this project is collected using the script:
* `00_2021_censusScraper.ipynb`
* `01_OSM_data_collection.ipynb`
* `02_satellite_image_explore.ipynb`

Collectively, these script exports data in a range of format. These are stored in the directory of `./data`, `./img`, or `./satellite`, including:
* MSOA shapefile in `.geojson` 
* Supermarket location in `.geojson`
* ONS census data in `.csv` 
* Rural urban classifcation in `.csv`
* Landsat-9 Satellite image in `.tif`

**please note that this list is not exhaustive.** Where some of the API request processes become infeasible due to time constraint, the corresponding data may be downloaded in a different format from the same source.

The specification for food desert is defined in:
* `04_food_desert_spec.ipynb`
* `05_matrix_indisctor_exploration.rmd`

The python script is used to compute supermarket aggregate, that mainly requires the processing of shapefile. The R markdown script is developed specifically for computing that involves geospatial data stored in the raster format.



