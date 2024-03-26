README for Step2_NRT_FeatureValueExtraction_SubareaClassification

Overview
Land Cover Predictions Using the Random Forest Model
This script focuses on predicting land cover classes for specified subareas using calculated spectral indices and a Random Forest model. It involves reading values from spectral indices for grid points, saving these values as CSV files, predicting land cover classes, and converting the prediction results from CSV files into GeoTIFF format.

Requirements
Python 3.x
Libraries: os, time, rasterio, gc, re, pandas, pickle, sklearn, shapely, numpy, datetime, geocube, geopandas, warnings
Pre-calculated spectral indices for subareas
Random Forest models saved as .sav files

Installation
Ensure Python 3.x is installed on your system. Install the required Python libraries using pip:
pip install rasterio pandas scikit-learn shapely numpy geocube geopandas

Usage
Step 1: Extract Data for Prediction
1. Reads values from spectral indices for grid points within specified subareas and saves the data as CSV files.

Step 2: Predict Land Cover Classes
1. Uses Random Forest models to predict land cover classes for each grid point in the subareas. Predictions are saved as CSV files.

Step 3: Convert Predictions to GeoTIFF
1. Converts the prediction results from CSV files to GeoTIFF format, allowing for easy visualization and further analysis.

Key Functionalities
Data Extraction: Automates the process of reading spectral index values for grid points and prepares the data for predictions.
Prediction: Utilizes Random Forest models to perform land cover classification based on the extracted data.
Conversion to GeoTIFF: Transforms prediction results into a spatial format compatible with GIS software.

Output
CSV Files with Predictions: Contains the predicted land cover classes for grid points within the subareas.
GeoTIFF Files: Spatial representation of the prediction results, suitable for visualization and analysis in GIS applications.

Additional Notes
Before running the script, ensure all paths (for shapefiles, base TIFF folder, output CSV folder, and model folder) are correctly set according to your directory structure.
The project is designed to handle multiple subareas and time periods, making it flexible for a wide range of land cover prediction tasks.
Warnings from the sklearn library are suppressed to improve the readability of the script's output. However, you should be aware of how your version of sklearn interacts with the data and models used.