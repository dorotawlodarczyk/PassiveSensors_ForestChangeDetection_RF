README for Step11_StatisticsCalculation

Overview
Calculating Land Cover Classification Statistics for Specific Regions
This script is designed to calculate and record statistics of land cover classifications within specified regions. Leveraging raster data representing land cover classifications and vector boundaries from shapefiles, it computes the area and percentage share of each land cover class within the defined boundaries. The statistics are saved to text files, providing detailed insights for each region.

Requirements
Python 3.x
Libraries: os, rasterio, geopandas, numpy
Land cover classification raster file (.tif)
Region boundary shapefiles (.shp)

Installation
Ensure Python 3.x is installed on your system. Install the required Python libraries using pip:
pip install rasterio geopandas numpy

Usage
1. Prepare Data: Place your land cover classification raster file and shapefiles for the regions of interest in designated directories.
2. Configure Paths: Update the folder_path, file_name, shp_files, and output_folder_path variables in the script to point to the correct directories and files.
3. Execute Script: Run the script to generate land cover classification statistics for the specified regions. Statistics will include total area in square meters and square kilometers, and the percentage share of each land cover class.
4. Review Results: Check the output_folder_path directory for text files containing the computed statistics for each region.

Key Functionalities
Reading Raster Data: Opens and reads land cover classification raster files.
Applying Masks: Uses vector boundaries from shapefiles to mask the raster data, isolating the regions of interest.
Computing Statistics: Calculates the area (in m² and km²) and percentage share of each land cover class within the masked regions.
Saving Results: Outputs the statistics to text files, one for each region.

Output
Text Files: Each containing detailed land cover classification statistics for a specific region, saved in the output_folder_path.

Additional Notes
Ensure the coordinate reference system (CRS) of the raster data matches that of the shapefiles for accurate area calculations.
Modify the calculate_statistics function to adjust the level of detail or to include additional statistics as required.
The script can be extended to process multiple raster files or to iterate over a directory of shapefiles for batch processing.