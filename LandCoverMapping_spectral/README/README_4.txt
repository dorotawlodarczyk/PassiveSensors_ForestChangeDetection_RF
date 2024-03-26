README for Step4_AOIDivisionIntoSubareas

Overview
Tiling a Geographic Area into Fixed Size Squares
This script involves segmenting a large geographic area into manageable square tiles of fixed size using GeoPandas and Shapely. It aims to facilitate the detailed analysis or processing of extensive areas by breaking them down into smaller, more manageable units. The script reads a shapefile representing the area boundaries and divides it into square tiles, saving each intersecting tile as a new shapefile.

Requirements
Python 3.x
Libraries: geopandas, shapely, os
A shapefile (.shp) representing the geographic area boundaries

Installation
Ensure Python 3.x is installed on your system. Install the required Python libraries using pip:
pip install geopandas shapely

Usage
Dividing a Geographic Area into Square Tiles
1. The script reads the input shapefile to determine the geographical extent of the area.
2. It then iterates over the area, creating square tiles of 40,000 meters on each side.
3. For each tile that intersects with the area defined in the input shapefile, a new shapefile representing that tile is saved.

Key Functionalities
Geographic Area Segmentation: Efficiently divides a large geographic area into square tiles for easier handling and analysis.
Geometry Operations: Utilizes Shapely for creating square tiles and GeoPandas for spatial operations and to handle geospatial data.
Shapefile Output: Saves intersecting tiles as new shapefiles, preserving the geographic information system (GIS) format for further use.

Output
Tile Shapefiles: A series of shapefiles, each representing a square tile that intersects with the input shapefile's geographic area. These are saved in a specified output directory.

Additional Notes
Before running the script, ensure the input_shapefile path is correctly set to the location of your area boundaries shapefile, and the output_folder is set to your desired directory for saving the tile shapefiles.
The tile size is adjustable. The default size is set to 40,000 meters by 40,000 meters but can be modified based on specific requirements.
This process is designed for efficiency but may require adjustments depending on the size and complexity of the input geographic area.