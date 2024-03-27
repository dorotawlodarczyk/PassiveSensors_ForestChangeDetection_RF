# Overview of the Project 

This project involves a comprehensive workflow for acquiring, processing, and analyzing satellite imagery from Landsat-8 and Sentinel-2 for land cover classification and change detection. The process includes searching for satellite images within specific geographic boundaries, calculating various spectral indices, validating forest cover predictions, and analyzing forest cover changes over time. The project leverages Python and several libraries such as GeoPandas, Rasterio, and Scikit-learn, among others, to handle geospatial data, perform raster operations, and apply machine learning techniques for classification tasks.

### Workflow Components

#### Land Cover Mapping (`LandCoverMapping_spectral`)
- **Objective**: Perform large-scale land cover classification using Sentinel-2 and Landsat-8 imagery.
- **Features**:
  - Automated satellite image acquisition based on geographic, temporal, and cloud cover criteria.
  - Calculation of spectral indices to evaluate vegetation health and land cover characteristics.
  - Land cover classification using Random Forest models.
  - Model accuracy assessment against ground truth data.
    ![Schemat workflow](https://github.com/dorotawlodarczyk/PassiveSensors_ForestChangeDetection_RF/blob/main/graphs/LandCoverMapping_spectral.jpg?raw=true)

#### Near-Real-Time Forest Change Detection (`NRT_ForestUpdate_spectral`)
- **Objective**: Provide detailed and timely updates on forest cover changes within specific subareas.
- **Features**:
  - Rapid image acquisition for designated subareas.
  - Automated extraction of spectral index values and application of Random Forest models for land cover classification.
  - Validation of classification accuracy and detailed analysis of forest gain and loss.
- **Implementation Note**: For full functionality of the NRT codes, it is essential to implement the following codes from the `LandCoverMapping_spectral` folder as part of the workflow: `Step4_AOIDivisionIntoSubareas.ipynb`, `Step5_GRIDCreation.ipynb`, and `Step7_RandomForestModelBuilding.ipynb` according to the provided workflow schema.
 ![Schemat workflow](https://github.com/dorotawlodarczyk/PassiveSensors_ForestChangeDetection_RF/blob/main/graphs/NRT_ForestUpdate_spectral.jpg?raw=true)

## Installation and Usage

- Ensure Python 3.x is installed.
- Install the required libraries using pip: `pip install geopandas rasterio shapely numpy scikit-learn matplotlib seaborn eodag folium pandas geojson rioxarray gc shutil re`.
- Configure paths to input data (shapefiles and satellite images) and output directories as per the individual script requirements.
- Execute scripts according to the project workflow, starting from image acquisition and proceeding through spectral index calculation, classification, accuracy assessment, and change detection analysis.

## Additional Notes

- Modify search criteria, spectral indices calculations, and classification parameters according to the specific needs of your analysis.
- Monitor system resources when processing large datasets or high-resolution images.
- Ensure the coordinate reference systems (CRS) of all geospatial data used are compatible.

## Output

- **Interactive Maps**: Visualizing satellite image search results and geographic footprints.
- **TIFF Files**: Raster files for calculated spectral indices, classification results and forest change maps.
- **CSV and Text Files**: Summarizing accuracy assessments, classification metrics, and forest cover change statistics.

This project exemplifies the integration of remote sensing, GIS, and machine learning for environmental monitoring and analysis. It is adaptable for various applications such as agricultural monitoring, urban planning, and ecosystem conservation.
