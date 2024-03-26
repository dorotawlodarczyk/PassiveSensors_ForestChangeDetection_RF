README for Step12_GainLossAnalysis

Overview
Analyzing Forest Change Using Satellite Imagery
This script is designed for environmental scientists and GIS analysts to analyze forest cover changes over time by comparing two satellite images. Utilizing raster operations, it identifies areas of forest loss and gain between two time periods, calculates the area of these changes in square meters, and outputs both a change map and a detailed report. This tool is valuable for monitoring deforestation, reforestation, or afforestation activities within a specific region.

Requirements
Python 3.x
Libraries: rasterio, numpy

Installation
Ensure Python 3.x is installed on your system. Install the required Python libraries using pip:
pip install rasterio numpy

Usage
1. Prepare Satellite Images: Ensure you have two raster images representing land cover classifications for two different time periods. The images must be aligned and have the same dimensions and resolution.
2. Configure File Paths: Update the first_file, second_file, output_file, and txt_output_file variables in the script to point to your first and second period raster files, the desired location for the change map output, and the text report summarizing forest change statistics.
3. Run the Script: Execute the script to compare the two satellite images, identify changes in forest cover, and calculate the areas of loss and gain.
4. Review Outputs: Check the specified output directory for the change map raster file and the text file report. The change map will visually represent forest loss and gain, while the report will detail the total area of each.

Key Functionalities
Forest Change Detection: Identifies areas where forest cover has been lost or gained between two time periods.
Area Calculation: Computes the area (in square meters) of forest loss and gain based on the pixel size of the satellite images.
Change Map Generation: Produces a change map highlighting areas of forest loss and gain.
Detailed Reporting: Generates a text report summarizing the total area of forest loss, gain, and net change.

Output
Change Map (.tif): A raster file visually representing areas of forest loss (coded as 1) and gain (coded as 2).
Forest Change Report (.txt): A text file detailing the total area of forest loss, gain, and the net change in square meters.

Additional Notes
The classification raster images should use a consistent land cover classification scheme, where a specific value represents forested areas (e.g., 6 for forest).
The pixel size for area calculations (default is 400 m² for 20m x 20m pixels) can be adjusted to match the resolution of your raster data.
Ensure the raster images and shapefiles are in the same coordinate reference system (CRS) for accurate analysis.