README for Step5_NRT_GainLossAnalysis

Overview
Forest Gain and Loss Determination 
This script utilizes Sentinel-2 satellite imagery to analyze changes in forest cover over time within specified areas of interest (AOIs). By comparing satellite imagery taken at two closest dates, the project identifies areas of forest loss and gain, calculates the corresponding areas in square meters, and generates change maps for a detailed visual representation of forest cover changes.

Requirements
Python 3.x
Libraries: rasterio, numpy, os, re, datetime

Installation
Ensure Python 3.x is installed on your system. Install the required Python libraries using pip:
pip install rasterio numpy

Usage
Determining Forest Gain and Loss
1. Processes TIFF files representing satellite imagery of specified subareas.
2. Analyzes changes between the two closest dates with high classification accuracy to determine areas of forest loss and gain.
3. Generates change maps indicating areas of loss and gain, and calculates the total area for each change type.

Key Functionalities
Raster Data Processing: Reads and compares raster data from TIFF files to identify changes in forest cover.
Change Detection: Identifies pixels representing forest loss and gain between two time points.
Area Calculation: Calculates the total area (in square meters) affected by forest loss and gain based on pixel counts.
Change Map Generation: Creates change maps showing areas of forest loss and gain for visual assessment and further analysis.
Summary Reporting: Writes a summary of forest loss and gain, including total areas affected, to a text file for documentation and reference.

Output
Change Maps: TIFF files visualizing the areas of forest loss (marked as 1) and gain (marked as 2) for each AOI between the two closest dates.
Summary File: A text file summarizing the results of the analysis, including total areas of forest loss and gain for each AOI.

Additional Notes
Before running the script, ensure that input_folder, tiles_accuracy_file, output_folder, and summary_file_path are set to the correct paths according to your project directory structure.
The script filters satellite images based on their classification accuracy for forest (class 6) using an F1-score threshold of 0.8, ensuring that only high-accuracy images are used for change detection.
The pixel size for area calculation is assumed to be 20m x 20m (400m^2 per pixel). Adjust the pixel_size parameter in the calculate_area function if using imagery with a different resolution.
