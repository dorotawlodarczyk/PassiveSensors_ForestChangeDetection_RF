README for Step1b_NRT_L-8_DataAcquisition_IndicatorCalculation

Overview
Landsat-8 Data Search and Spectral Indices Calculation
This script facilitates the acquisition of Landsat-8 satellite imagery, covering specific geographic areas within a specified timeframe and cloud cover limit. It includes processes for searching and downloading imagery, resampling images to match a reference image, and calculating various spectral indices for areas of interest.

Requirements
Python 3.x
Libraries: eodag, geopandas, shapely, matplotlib, datetime, collections, itertools, logging, os, numpy, rioxarray, rasterio, gc, shutil, re
Landsat-8 satellite images within the specified date range and cloud cover

Installation
Ensure Python 3.x is installed on your system. Install the required Python libraries using pip:
pip install eodag geopandas shapely matplotlib datetime collections itertools logging os numpy rioxarray rasterio gc shutil re

Usage

Part 1: Search for Full Coverage of Designated Subareas
1. Searches for Landsat-8 images that fully cover specified subareas within a given date range and cloud cover limit.
2. Generates a heatmap visualizing the number of image sets fully covering each area.

Part 2: Download the Images
1. Searches for and downloads unique Landsat 8 imagery IDs from a specified text file.
2. Utilizes EODataAccessGateway (EODAG) to interface with a preferred data provider for the download process.

Part 3: Resampling
1. Resamples Landsat 8 raster images to match the resolution and alignment of a reference image.
2. Preserves the folder structure while saving the resampled images.

Part 4: Calculation of Spectral Indices
1. Automates the processing of Landsat 8 satellite imagery by clipping, merging, and calculating various spectral indices for areas of interest.

Key Functionalities
Data Acquisition: Utilizes EODataAccessGateway for searching and downloading Landsat-8 imagery.
Image Processing: Includes resampling of images to a common resolution and alignment, as well as clipping to match specific area boundaries.
Spectral Indices Calculation: Supports multiple indices such as NDVI, GNDVI, EVI, SAVI, among others, facilitating a wide range of environmental and agricultural analyses.

Output
Heatmap Image: Visualizes the number of image sets that fully cover each designated subarea.
Downloaded Landsat-8 Imagery: Stored in the specified output directory.
Resampled Images: Aligned and resampled images saved with preserved folder structure.
Spectral Indices TIFFs: Calculated spectral indices saved as TIFF files for further analysis.

Additional Notes
The project is modular, allowing users to customize the process to their specific requirements, such as adjusting the cloud cover limit, date range, or spectral indices to be calculated.
Ensure that all paths (for area boundaries, text file location, output files save location, etc.) are correctly set before executing the scripts.