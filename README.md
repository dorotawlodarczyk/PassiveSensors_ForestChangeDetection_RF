# Overview of the Project

This project involves a comprehensive workflow for acquiring, processing, and analyzing satellite imagery for land cover classification and change detection. The process includes searching for satellite images within specific geographic boundaries, calculating various spectral indices, validating forest cover predictions, and analyzing forest cover changes over time. The project leverages Python and several libraries such as GeoPandas, Rasterio, and Scikit-learn, among others, to handle geospatial data, perform raster operations, and apply machine learning techniques for classification tasks.

## Key Components

1. **Sentinel-2 and Landsat-8 Image Acquisition**: Automated search and download of Sentinel-2 and Landsat-8 satellite images based on specified criteria such as geographic area, time frame, and cloud cover.

2. **Spectral Indices Calculation**: Processing of satellite imagery to calculate indices like NDVI, GNDVI, EVI, SAVI, and more, which are crucial for environmental and vegetation analysis.

3. **Image Resampling and Mosaicking**: Alignment and stitching of satellite images to create a consistent and comprehensive view of the target area.

4. **Land Cover Classification**: Application of Random Forest classifiers to predict land cover classes based on the calculated spectral indices.

5. **Accuracy Assessment and Validation**: Evaluation of classification accuracy using ground truth data and calculation of metrics such as F1-score, precision, recall, and Cohen's Kappa.

6. **Forest Cover Change Detection**: Analysis of changes in forest cover by comparing satellite imagery over time, identifying areas of forest loss and gain, and calculating the area affected by these changes.

7. **Output Generation**: Creation of change maps, accuracy assessment reports, and statistical summaries to visualize and document the findings.

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
- **TIFF Files**: Raster files for calculated spectral indices and classification results.
- **CSV and Text Files**: Summarizing accuracy assessments, classification metrics, and forest cover change statistics.

This project exemplifies the integration of remote sensing, GIS, and machine learning for environmental monitoring and analysis. It is adaptable for various applications such as agricultural monitoring, urban planning, and ecosystem conservation.
