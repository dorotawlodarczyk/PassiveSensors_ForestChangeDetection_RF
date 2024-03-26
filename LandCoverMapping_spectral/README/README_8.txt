README for Step8_SubareaClassification

Overview
Spatial Data Prediction (GRID Point Classification for Subareas)
This script facilitates spatial data prediction by leveraging a pre-trained Random Forest model to classify geographical features based on their attributes. It involves reading CSV files containing feature values and geometries, preprocessing the data (including imputation of missing values and feature scaling), applying the pre-trained model to predict classifications for each spatial feature, and saving the prediction results to new CSV files.

Requirements
Python 3.x
Libraries: os, time, geopandas, pandas, rasterio, shapely, pickle, numpy, sklearn
Pre-trained Random Forest model saved as .sav
CSV files with geographical features and their geometries

Installation
Ensure Python 3.x is installed on your system. Install the required Python libraries using pip:
pip install geopandas pandas rasterio shapely numpy scikit-learn

Usage
Predicting Classifications for Spatial Features
1. Iterates through CSV files containing feature values and geometries.
2. Performs data preprocessing to prepare the dataset for prediction.
3. Applies the pre-trained Random Forest model to predict classifications for each feature.
4. Saves the prediction results to new CSV files in a specified output directory.

Key Functionalities
Data Preprocessing: Handles missing values with median imputation and applies feature scaling to normalize the dataset.
Model Prediction: Utilizes a pre-trained Random Forest model to classify spatial features based on their attributes.
Result Saving: Outputs the prediction results alongside geometries to new CSV files for further analysis or visualization.

Output
Prediction Result CSV Files: Each processed input CSV file corresponds to a new CSV file containing the original geometries and predicted classifications, stored in the specified output directory.

Additional Notes
Before running the script, ensure the paths for csv_folder, result_csv, and the location of the pre-trained Random Forest model (RF_model.sav) are correctly set.
The prediction process may require adjustments based on the specific characteristics of your dataset, such as the selection of features for prediction or the handling of special cases in the data.
Ensure that the coordinate reference system (CRS) used in the GeoDataFrame matches the CRS of your spatial data for accurate geometric operations.
