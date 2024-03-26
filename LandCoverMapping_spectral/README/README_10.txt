README for Step10_AccuracyAssessment

Overview
Spatial Analysis and Accuracy Assessment of Classified Imagery
This script entails a two-part process designed for geospatial analysis and accuracy assessment of classified satellite imagery. The first part involves extracting classification results against validation samples to generate accuracy assessment CSV files. The second part delves deeper by calculating various accuracy metrics and visualizing the model's performance. Utilizing libraries such as GeoPandas, Rasterio, and Matplotlib, this project ensures CRS compatibility checks and leverages Python's data science ecosystem for geospatial data handling and analysis.

Requirements
Python 3.x
Libraries: GeoPandas, Pandas, Numpy, Matplotlib, Rasterio, Shapely, Seaborn, Scikit-learn, Pickle
Pre-processed and classified raster files (.tif)
Validation samples as shapefiles (.shp)
Pre-trained Random Forest model (optional for the second part)

Installation
Ensure Python 3.x is installed. Install the required libraries using pip:
pip install geopandas pandas numpy matplotlib rasterio shapely seaborn scikit-learn

Usage
Part 1: Spatial Analysis and Accuracy Assessment
1. Processes shapefiles containing validation samples and raster files of classified imagery.
2. Extracts spatial coordinates from the shapefiles and retrieves corresponding classifications from the raster files.
3. Compares these classifications to generate accuracy assessment CSV files.

Part 2: Automated Accuracy Analysis and Reporting
1. Processes the generated CSV files to calculate accuracy metrics such as F1-scores, Cohen's Kappa, overall accuracy, and AUC for ROC curves.
2. Generates confusion matrices and ROC curve plots for visualization.
3. Outputs detailed accuracy reports including class-wise metrics to a text file.

Output
Accuracy Assessment CSV Files: Contain predicted and actual classifications along with spatial coordinates.
Accuracy Report: A comprehensive report detailing various accuracy metrics, saved as a text file.
Visualizations: Confusion matrices and ROC curve plots for each class, saved in specified directories.

Key Functionalities
Validation against Ground Truth: Aligns prediction results with validation samples for accuracy assessment.
Metric Calculation: Utilizes advanced statistical methods to compute accuracy metrics, offering insights into the model's performance.
Visualization: Generates graphical representations of the model's accuracy, facilitating easier interpretation of results.

Additional Notes
Ensure paths for shapefile folders (shp_folders), raster file folder (tif_folder), and output directories (output_folder and confusion_matrix_folder) are correctly configured.
The CRS of the shapefiles and raster files should match or be compatible for accurate spatial analysis.
Adjustments to the model or analysis parameters might be required based on the specific characteristics of the dataset or the project goals.
