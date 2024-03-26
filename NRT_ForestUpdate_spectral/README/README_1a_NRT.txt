README for Step1a_NRT_S-2_DataAcquisition_IndicatorCalculation

Overview
Sentinel-2 Data Acquisition and Spectral Indices Calculation
This script aims to streamline the process of acquiring Sentinel-2 satellite imagery and calculating various spectral indices for specified subareas. It is divided into two main parts: 1) Search for full coverage of designated subareas, and 2) Calculation of spectral indices for those subareas.

Requirements
Python 3.x
Libraries: eodag, geopandas, shapely, matplotlib, re, os, rasterio, numpy, shutil, subprocess, time
Sentinel-2 satellite images for the specified date range and cloud cover
Installation
Ensure Python 3.x is installed on your system. Install the required Python libraries using pip:
pip install eodag geopandas shapely matplotlib re os rasterio numpy shutil subprocess time

Usage

Part 1: Search for Full Coverage of Designated Subareas
This part searches for Sentinel-2 satellite images that fully cover specified subareas within a given date range and cloud cover limit.
It generates a text file listing the unique image sets per tile and a heatmap visualizing the coverage frequency of these images across the subareas.

Key Steps:
1. Initialize EODataAccessGateway and search parameters.
2. Iterate over subareas and search for images meeting the criteria.
3. Determine full coverage by checking if individual or combined images completely cover the subareas.
4. Generate a text file listing the unique image sets per tile.
5. Produce a heatmap visualizing the coverage frequency.

Part 2: Calculation of Spectral Indices
This part processes the satellite imagery by clipping spectral bands to specific subarea boundaries, merging images, and calculating various spectral indices.

Key Steps:
1. Generate image paths based on the text file created in Part 1.
2. Find JP2 files for required spectral bands within image directories.
3. Clip and save spectral bands to subarea boundaries.
4. Merge images if necessary to cover the entire subarea.
5. Calculate multiple spectral indices like NDVI, GNDVI, EVI, SAVI, and others for areas of interest.

Output
Part 1: A text file with listed unique image sets per tile and a heatmap image file visualizing the coverage frequency.
Part 2: Spectral indices calculated for specified subareas, saved as TIFF files.

Additional Notes
The scripts utilize functionality from multiple Python libraries to process geospatial data and satellite imagery.
Ensure all paths (to area boundaries, text file save location, output files save location, and initial folder for image search) are correctly set in the script before execution.
The processing part is designed to be flexible, allowing for the addition or modification of spectral indices calculations as required.
