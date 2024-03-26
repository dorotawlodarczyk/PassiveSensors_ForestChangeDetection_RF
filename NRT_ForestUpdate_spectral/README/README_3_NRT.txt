README for Step3_NRT_ValidationFeatureValueExtraction

Overview
Forest Cover Validation Points Feature Extraction
This script processes satellite imagery to validate forest cover predictions by comparing raster data from .tif files with validation points stored in a .shp file. The validation process involves extracting feature values at specified validation points and saving these values alongside the target classes to CSV files for further analysis.

Requirements
Python 3.x
Libraries: os, geopandas, pandas, rasterio, shapely, time

Installation
Ensure Python 3.x is installed on your system. Install the required Python libraries using pip:
pip install geopandas pandas rasterio shapely

Usage
Validation Points Feature Extraction
2. Reads raster data from .tif files and validation points from a .shp file.
3. For each .tif file, extracts feature values at the locations specified by the validation points.
4. Saves the extracted feature values, along with the target classes from the .shp file, to CSV files.

Key Functionalities
Data Reading: Opens and reads the spatial extent of raster (.tif) files and the geographic locations of validation points (.shp file).
Feature Extraction: For each validation point within the bounds of a raster file, extracts the corresponding raster value.
Result Compilation: Compiles the target class and predicted feature value for each validation point into a pandas DataFrame, which is then saved as a CSV file.

Output
CSV Files: For each .tif file processed, a corresponding CSV file is generated, containing the geometry of each validation point, its target class, and the predicted feature value extracted from the raster file.

Additional Notes
Before running the script, ensure the paths for the shapefile folder (shp_folder), the output folder (output_folder), and the TIFF folder (tif_folder) are correctly set according to your file structure.
The USE_PYGEOS environment variable is set to '0' to avoid compatibility issues. This can be adjusted based on your system's configuration and the versions of the libraries you are using.
This process is designed to handle multiple .tif files, making it scalable for large datasets.