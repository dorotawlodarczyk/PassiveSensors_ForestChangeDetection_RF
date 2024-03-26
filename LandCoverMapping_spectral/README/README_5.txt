README for Step5_GRIDCreation

Overview
Generating Grid Points Within Shapefile Boundaries
This script automates the generation of a grid of points within the boundaries of each shapefile located in a specified input folder. By iterating over shapefiles, the script calculates and filters a grid of points based on a predefined pixel size, ensuring points fall within the shapefile's geometries. The output, a set of GeoDataFrames containing these points, is then saved as new shapefiles in a designated output folder. This process is valuable for spatial analysis, sampling within geographic areas, or preparing data for further geospatial processing tasks.

Requirements
Python 3.x
Libraries: os, geopandas, shapely
Input shapefiles (.shp) representing geographic areas

Installation
Ensure Python 3.x is installed on your system. Install the required Python libraries using pip:
pip install geopandas shapely

Usage
Generating and Saving Grid Points
1. Walks through the specified input folder to find and process shapefiles.
2. For each shapefile, generates a grid of points spaced according to the specified pixel size.
3. Saves the grid points that fall within the shapefile's geometries to a new shapefile in the output folder.

Key Functionalities
Shapefile Processing: Identifies and reads shapefiles within the input folder, setting an appropriate coordinate reference system (CRS) for spatial operations.
Grid Points Generation: Calculates a grid of points based on the pixel size and the shapefile's bounding box, ensuring the points align with the shapefile's spatial extent.
Spatial Filtering: Filters out points that do not intersect with the shapefile's geometries, ensuring accuracy and relevance of the generated points.
Output Saving: Saves the filtered grid points as new shapefiles, maintaining the geospatial data format for compatibility with GIS software and further analysis.

Output
Grid Point Shapefiles: Each processed input shapefile corresponds to a new shapefile containing a grid of points within its boundaries, saved in the specified output folder.

Additional Notes
Ensure the input_folder and output_folder paths are correctly set to your directory structure before running the script.
The pixel_size determines the spacing of the grid points. Adjust this value based on the desired resolution or specific requirements of your spatial analysis.
The script sets the CRS of each shapefile to "EPSG:32631". Modify the CRS assignment as necessary to match your geospatial data's projection system.