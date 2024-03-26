README for Step9_SubareaConnection

Overview
Conversion of CSV Prediction Results to GeoTIFF and Merging TIFF Files
This script involves two main processes: converting CSV files containing predicted classifications and spatial coordinates to GeoTIFF raster files for spatial analysis and visualization, and merging multiple TIFF files into a single TIFF file for GIS applications. The first part uses GeoPandas, Shapely, and the geocube library to transform CSV data into geospatial dataframes and exports them as GeoTIFFs. The second part employs GDAL to merge these GeoTIFF files into a comprehensive raster file.

Requirements
Python 3.x
Libraries: os, time, pandas, geopandas, shapely, geocube, osgeo (GDAL), glob, subprocess
CSV files with prediction results and spatial coordinates
GDAL installed on the system

Installation
Ensure Python 3.x is installed on your system. Install the required Python libraries using pip:
pip install pandas geopandas shapely geocube
GDAL installation varies based on the operating system. Please refer to the GDAL documentation for installation instructions.

Usage
Part 1: Converting CSV to GeoTIFF
1. Iterates through specified CSV files containing prediction results.
2. Converts CSV data into geospatial dataframes and exports as GeoTIFF files.

Part 2: Merging TIFF Files
1. Collects TIFF files from a specified directory.
2. Merges them into a single TIFF file using a GDAL command.

Key Functionalities
CSV to GeoTIFF Conversion: Transforms spatial prediction results from CSV format into GeoTIFF, enabling GIS applications and spatial visualization.
TIFF Merging: Combines multiple GeoTIFF files into a single file for easier management and analysis in GIS software.

Output
GeoTIFF Files: Raster files for each processed CSV, stored in the specified output directory.
Merged TIFF File: A comprehensive raster file merging all individual GeoTIFFs.

Additional Notes
Before executing the scripts, ensure the paths for csv_folder, result_tif, and the GDAL command (gdal_merge.py) are correctly configured according to your system setup.
The pixel size for GeoTIFF generation and the merging process can be adjusted based on project requirements or spatial resolution preferences.
Ensure that the coordinate reference system (CRS) used matches the spatial data specifications for accurate geographic representation.