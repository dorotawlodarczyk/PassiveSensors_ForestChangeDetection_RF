README for Step6_FeatureValueExtraction 

Overview
Feature Value Extraction from Raster Data
This script automates the extraction of feature values from raster files (.tif) based on coordinates defined in shapefiles (.shp). The process involves reading shapefiles to obtain geographic coordinates, extracting corresponding raster values from a series of TIFF images, and saving the cleaned, aggregated data into CSV files. This workflow is particularly useful for spatial data analysis, allowing for the integration of raster data into statistical models, visualization tools, or geographic information systems (GIS) for further analysis.

Requirements
Python 3.x
Libraries: os, time, geopandas, rasterio, numpy, gc (garbage collection)
Input directories containing shapefiles and corresponding raster files

Installation
Ensure Python 3.x is installed on your system. Install the required Python libraries using pip:
pip install geopandas rasterio numpy

Usage
Extracting Feature Values
1. Iterates through shapefiles in a specified directory, using each shapefile to extract feature values from raster files within another specified directory.
2. Cleans the extracted data by removing entries with missing values.
3. Saves the cleaned data to CSV files in a specified output directory.

Key Functionalities
Shapefile Processing: Reads geographic coordinates from shapefiles to define the locations for raster value extraction.
Raster Data Handling: Utilizes rasterio to access and sample raster data based on the coordinates from shapefiles.
Data Cleaning and Saving: Filters out incomplete data entries and saves the cleaned data into CSV files for each shapefile processed.

Output
CSV Files: For each shapefile processed, a corresponding CSV file is generated containing the extracted feature values, cleaned of any missing data. These files are stored in the specified output directory.

Additional Notes
Before running the script, ensure the paths for shp_folder, tif_folder, and output_csv_folder are correctly set to the locations of your input shapefiles, input raster files, and desired output CSV files, respectively.
The pixel size or spatial resolution of the raster files and the density of the points in the shapefiles should be considered to ensure accurate feature value extraction.
This script is optimized for efficiency, including the use of garbage collection to manage memory usage during processing. However, processing time and resource utilization may vary based on the size and number of input files.