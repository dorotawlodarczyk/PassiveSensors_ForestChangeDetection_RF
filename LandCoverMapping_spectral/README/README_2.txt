README for Step2_SpectralIndicatorMosaicking

Overview
Converting and Merging TIFF Files with Nodata Value Adjustment
This script involves processing a batch of TIFF files to adjust their no-data values and subsequently merging them into a single TIFF file. Utilizing the GDAL library for raster data manipulation and numpy for array operations, the script identifies zero values within each TIFF file, converts them to a specified no-data value, and merges the adjusted files. This process is essential for consistent no-data value handling across multiple geospatial datasets and for creating a unified raster file for analysis or visualization purposes.

Requirements
Python 3.x
Libraries: osgeo (GDAL), numpy, os, subprocess
GDAL installed on the system (including gdal_merge.py script)
A collection of geospatial raster data in TIFF format

Installation
Ensure Python 3.x and GDAL are installed on your system. GDAL provides the necessary tools for raster data manipulation beyond what's available through pip. Install the required Python library using pip:
pip install numpy
For GDAL installation, refer to the official GDAL documentation: https://gdal.org/download.html

Usage
Converting Zero Values to Nodata and Merging TIFF Files
1. Reads each TIFF file from a specified directory, adjusting zero values to a predefined no-data value (-9999).
2. Utilizes GDAL to read, modify, and write the adjusted raster data.
3. Merges the adjusted TIFF files into a single file using gdal_merge.py.

Key Functionalities
Zero Value Adjustment: Identifies and converts zero values within TIFF files to a specified no-data value, ensuring consistency across datasets.
File Merging: Combines multiple adjusted TIFF files into a single raster file, facilitating further geospatial analysis or visualization.

Output
Adjusted TIFF Files: A series of TIFF files with zero values converted to the specified no-data value, saved in the same directory with a modified filename.
Merged TIFF File: A single TIFF file resulting from the merging of all adjusted files, stored at a specified location.

Additional Notes
Before running the script, ensure the tif_folder path is correctly set to the directory containing your TIFF files and output_file points to the desired location for the merged TIFF file.
The gdal_merge_path variable should point to the location of the gdal_merge.py script on your system. This script is typically included with GDAL installations.
This process modifies the original TIFF files. Consider creating backups before proceeding if original data preservation is necessary.