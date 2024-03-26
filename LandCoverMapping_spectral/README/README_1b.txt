README for Step1b_L-8_DataAcquisition_Resampling_IndicatorCalculation

Landsat-8 Image Search, Visualization, Resampling, and Indices Calculation

Overview
Landsat-8 Image Search, Visualization, Resampling, and Indices Calculation
This script provides a comprehensive workflow for dealing with Landsat-8 satellite imagery within specified geographical boundaries and time frames. It encompasses searching for and filtering satellite images based on criteria such as cloud cover and date range, visualizing the search area and selected satellite images on a map, resampling the images to match a reference image's spatial resolution, and calculating a variety of satellite image indices.

Requirements
Python 3.x
Libraries: eodag, os, folium, geopandas, pandas, geojson, rioxarray, rasterio, numpy
A shapefile (.shp) defining the geographic area of interest
Access to Landsat-8 satellite images

Installation
Ensure Python 3.x is installed on your system. Install the required Python libraries using pip:
pip install eodag folium geopandas pandas geojson rioxarray rasterio numpy

Usage
Part 1: Landsat-8 Image Search and Visualization
1. Uses the EODataAccessGateway (EODAG) to search for Landsat-8 satellite images within a defined geographic footprint, filtering the results by cloud cover and date range.
2. Visualizes the geographic footprint and the metadata of retrieved satellite images on an interactive map using Folium.

Part 2: Resampling and Saving Satellite Images
1. Resamples Landsat-8 satellite images to match the spatial resolution and coordinate reference system of a reference image using rioxarray and rasterio.
2. Saves the resampled images to a specified output directory.

Part 3: Automated Calculation and Saving of Various Satellite Image Indices
1. Processes the resampled satellite images to calculate multiple vegetation and water indices, including NDVI, GNDVI, EVI, SAVI, and others.
2. Saves the calculated indices as TIFF files in a structured directory for further analysis.

Key Functionalities
Satellite Image Search: Automates the search and selection of Landsat-8 images based on specific search criteria.
Image Visualization: Leverages Folium and GeoPandas to visualize the area of interest and the metadata of selected satellite images on an interactive map.
Image Resampling: Utilizes rasterio and rioxarray for spatial resampling of satellite images, aligning them with the spatial characteristics of a reference image.
Index Calculation: Employs numpy and rasterio to calculate and save a variety of satellite image indices that are crucial for environmental and vegetation analysis.

Output
Interactive Maps: Maps displaying the geographic footprint and metadata of selected satellite images.
Resampled Satellite Images: A set of resampled Landsat-8 images saved in the specified output directory.
Satellite Image Indices: TIFF files for each calculated spectral index, organized and saved in a designated folder.

Additional Notes
Before running the scripts, ensure the paths for shapefile_path, output_folder, and other directories are correctly set according to your file organization.
The workflow is designed to handle multiple satellite images and can process large datasets efficiently, but it's advisable to monitor system resources during the operation.
Make sure to have the correct access rights or API keys (if required) for the EODataAccessGateway (EODAG) to search for and download Landsat-8 satellite images.