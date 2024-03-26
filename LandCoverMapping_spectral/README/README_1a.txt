README for Step1a_S-2_DataAcquisition_IndicatorCalculation

Overview
Sentinel-2 Image Search and Spectral Indices Calculation
This script aims to facilitate the search for Sentinel-2 satellite images within specified geographic boundaries and time frames, filter these images by cloud cover, and calculate various spectral indices from the acquired images. The process involves visualizing the search results and area boundary on an interactive map and processing the satellite imagery to calculate indices such as NDVI, GNDVI, EVI, and others, saving the results as TIFF files.

Requirements
Python 3.x
Libraries: eodag, os, rasterio, numpy, folium, geopandas, gdal, gc, memory_profiler
Shapefile (.shp) containing geographic boundaries
Sentinel-2 satellite images

Installation
Ensure Python 3.x is installed on your system. Install the required Python libraries using pip:
pip install eodag rasterio numpy folium geopandas gdal memory_profiler

Usage
Part 1: Sentinel-2 Image Search
1. Uses the EODataAccessGateway from the eodag library to search for satellite images within specified boundaries and time frames.
2. Filters images by cloud cover and visualizes the search results and area boundary on an interactive map using Folium.

Part 2: Calculation of Spectral Indices
1. Processes satellite imagery to organize image files by resolution and spectral bands.
2. Calculates various vegetation and water indices from the images and saves the results as TIFF files in a specified output directory.

Key Functionalities
Image Search and Visualization: Automates the search for Sentinel-2 images, filtering by cloud cover and visualizing the geographical extent of the search results and specified area boundaries.
Spectral Indices Calculation: Utilizes rasterio and numpy to calculate indices such as NDVI, GNDVI, EVI, SAVI, OSAVI, DVI, SR, GEMI, NDWI, MNDWI, LSWI, UI, NDBI, MNDBI, and BSI from the satellite images, providing valuable insights into vegetation health, water content, and other environmental parameters.

Output
Interactive Map: A Folium map displaying the search results and area boundaries.
TIFF Files: A set of TIFF files for each calculated spectral index, saved in the specified output directory.

Additional Notes
Before running the scripts, ensure the shapefile_path, output_folder, and tif_folder paths are correctly set according to your directory structure.
The calculation of spectral indices is based on the presence of specific bands within the Sentinel-2 imagery. Ensure the images have the necessary bands for the indices you intend to calculate.
The process utilizes significant memory resources, especially when processing large numbers of images or high-resolution data. Monitor memory usage and adjust the processing batch size as necessary.
