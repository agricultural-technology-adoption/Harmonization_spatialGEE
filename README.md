# Harmonization_spatialGEE
# Adding geo-spatial data to survey data
## Overview

The sample script provides the data extraction and exportation code to add spatial information for geolocated data. A sample code and the base image loading functions are provided to allow users to adapt the code for their use. 

The code provides three levels of extraction:
* Pixel co-located with jittered GPS coordinates
* Spatial average over circular buffer with radius equal to jittering radius
* Spatial average over Admin 2 boundary

Google Colaboratory Notebook & Python interface to Google Earth Engine
* Open access, easily shareable, configurable
* Earth Engine -- maintained, high-level QC databases
* Folium maps -- interactive, can zoom and take snapshots of what you like for web, project materials, etc.
* Google Docs -- Documentation in easy web-based format

Extraction:
* Match coordinates and survey dates to raster data
* Reduce (average, sum, etc. over area, time)
* Export to CSV

Data sources used:
1. Luminosity; DMSP OLS: Nighttime Lights Time Series Version 4, Defense Meteorological Program Operational Linescan System
https://developers.google.com/earth-engine/datasets/catalog/NOAA DMSP-OLS NIGHTTIME LIGHTS Annual Level, from 1992-2013
2. Forest Cover; Hansen Global Forest Change v1.8 (2000-2020)
https://developers.google.com/earth-engine/datasets/catalog/UMD hansen global forest change 2020 v1 Annual Level, from 2000-2019
3. Soil Properties; SoilGrids250m 2.0 (Bulk density, Cation exchange capacity at pH7, Coarse fragments, Clay, Total Nitrogen, Organic carbon density, Organic carbon stock, pH in H2O, Sand, Silt, Soil organic carbon)
 https://git.wur.nl/isric/soilgrids/soilgrids.notebooks/-/blob/master/markdown/access on gee.md
Cross-Sectional Level
4. NDVI; USGS Landsat 8 Level 2, Collection 2, Tier 1
 https://developers.google.com/earth-engine/datasets/catalog/LANDSAT LC08 C02 T1 L2
Annual Level, from 2013-2022 Matched via GAUL 2015 Boundaries
5. Precipitation; CHIRPS Daily: Climate Hazards Group InfraRed Precipitation With Station Data (Version 2.0 Final)
https://developers.google.com/earth-engine/datasets/catalog/UCSB-CHG CHIRPS DAILY
Monthly Level, from January 1981-August 2022
6. Temperature; ERA5 Daily Aggregates – Latest Climate Reanalysis Produced by ECMWF / Copernicus Climate Change Service
https://developers.google.com/earth-engine/datasets/catalog/ECMWF ERA5 DAILY Monthly Level, from January 1979-June 2020

