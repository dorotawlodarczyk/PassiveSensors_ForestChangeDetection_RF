README for Step3_AOIClipping

Overview
This script streamlines the task of cropping GeoTIFF images to the boundaries defined by a shapefile. The crop_tiffs_to_shp function automates the cropping of multiple GeoTIFF images based on a shapefile's geometry, saving the cropped images to a designated output directory. This process is crucial for focusing geospatial analyses on specific areas of interest, ensuring data consistency, and efficiently managing spatial datasets.

Requirements
Python 3.x
Libraries: geopandas, os, rasterio, shapely, time, gc (garbage collection)
GeoTIFF images and a shapefile (.shp) defining the area to which the images will be cropped

Installation
Ensure Python 3.x is installed on your system. Install the required Python libraries using pip:
pip install geopandas rasterio shapely

Usage
Function: crop_tiffs_to_shp
1. Reads GeoTIFF images from a specified input directory and the geometry from a given shapefile.
2. Crops each GeoTIFF image to the shapefile's boundaries using rasterio's mask function.
3. Saves the cropped images to a specified output directory.

Key Functionalities
Automated Cropping: Processes all GeoTIFF images in a given directory, cropping them to the area defined by a shapefile.
Efficient Data Handling: Utilizes garbage collection to manage memory usage effectively, facilitating the processing of large datasets.
Time Tracking: Monitors and reports the time taken to complete the cropping process, providing insights into the efficiency of data processing.

Output
Cropped GeoTIFF Images: Each image processed by the function is cropped to the area defined by the shapefile and saved in the output directory, retaining the original spatial resolution and data integrity.

Additional Notes
Before running the script, ensure the input_folder_path, output_folder_path, and shapefile_path are correctly set to the locations of your GeoTIFF images, desired output directory, and shapefile, respectively.
The shapefile's geometry should be accurately defined and correspond to the spatial reference system of the GeoTIFF images to ensure precise cropping.
This script is designed to handle multiple images efficiently but may require adjustments based on the specific characteristics of your datasets, such as spatial resolution or file size.
