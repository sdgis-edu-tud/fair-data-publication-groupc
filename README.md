# Dataset title

## Table of Contents

- [1. GENERAL INFORMATION](#1-general-information)
- [2. METHODOLOGICAL INFORMATION](#2-methodological-information)
  - [2.1 Research questions, methods and envisioned uses](#21-research-questions-methods-and-envisioned-uses)
  - [2.2 Methods for processing the data](#22-methods-for-processing-the-data)
  - [2.3 Instrument- or software-specific information](#23-instrument--or-software-specific-information)
- [3. FILE OVERVIEW](#3-file-overview)
  - [3.1 File List](#31-file-list)
  - [3.2 Relationship between files](#32-relationship-between-files)
  - [3.3 File formats and naming conventions](#33-file-formats-and-naming-conventions)
- [4. DATA-SPECIFIC INFORMATION](#4-data-specific-information)
  - [4.1 Data](#41-data)
- [5. SHARING/ACCESS INFORMATION](#5-sharingaccess-information)
  - [5.1 Licenses/restrictions placed on the data](#51-licensesrestrictions-placed-on-the-data)
  - [5.2 Links to other resources](#52-links-to-other-resources)
  - [5.3 Recommended citation for this dataset](#57-recommended-citation-for-this-dataset)


# 1. GENERAL INFORMATION

## 1.1 Title of Dataset
Urban Stream Restoration Dataset of Teplica in Senica, Slovakia

## 1.2 Dataset description
This dataset contains quantitative data on normalization of 8 different MCDA aspects based on spatial geometry alongside stream Teplica, to show the suitability of areas to be prioritised in sustainable stream restoration efforts based on biodiversity, climate adaptation, and quality of life. Additional details about the project can be accessed [here](https://github.com/sdgis-edu-tud/report-asa2025-groupc).

## 1.3 Author Information
A. Principal Investigator  
- Name: Viola Ebermannová
- Institution: Technology University of Delft
- Address: Netherlands, Prague - Czechia
- Email: v.ebermannova@student.tudelft.nl

B. Associate or Co-investigator
- Name: Hongyue Kang
- Institution: Technology University of Delft
- Address: Zusterlaan 264b, Delft
- Email: hongyuekang@tudelft.nl

C. Associate or Co-investigator
- Name: Kelly Schoonderwoerd
- Institution: Technology University of Delft
- Address: Delft, Netherlands
- Email: K.R.Schoonderwoerd@student.tudelft.nl


## 1.4 Dates of data collection
- NDVI: 2025-05-12
- LST: 2025-06-06

## 1.5 Geographic location of data collection
Senica, Slovakia

## 1.6 Keywords
Sustainable stream restoration, regional ecological stability system, soil, NDVI, land surface temperature

## 1.7 Language
English

# 2. METHODOLOGICAL INFORMATION
## 2.1 Research questions, methods and envisioned uses
The research combines a lot of quantitative GIS-based spatial analysis with qualitative typological classification of land cover using Google Street View. By answering the research questiones on morphologically defined spatial units, this mixed-methods approach enables both a broad spatial overview and a detailed understanding of urban space alongside the Teplica in Senica (Slovakia).

### 2.1.1 Research question 1: How to improve local and supra local biodiversity resilience by interventions within the stream flood plain?
- Instrument 1 (quan): GIS-based spatial analysis 
- Instrument 2 (qual)：Typological analysis based on Google Street View 

### 2.1.2 Research question 2: How to use areas in the flood plain to capture water in the landscape?
- Instrument 1 (quan)：GIS-based spatial analysis 

### 2.1.3 Research question 3: What types of places should be created in the stream flood plain?
- Instrument 1 (quan)：GIS-based spatial analysis 

### 2.1.4 Envisioned uses of the dataset
- The dataset supports the prioritization of spatial units along the Teplica River in terms of their urgency for improvement in biodiversity, quality of life, and climate adaptation, thereby providing guidance for future spatial interventions.

## 2.2 Methods for processing the data
- NDVI: Sentinel-2 satellite imagery was accessed via Google Earth Engine (GEE), covering the study area during the growing season to ensure accurate vegetation representation.
The Normalized Difference Vegetation Index (NDVI) was calculated within GEE using the standard formula:
NDVI=(B8-B4)/(B8+B4)
where B8 represents the near-infrared (NIR) band and B4 represents the red band.
The resulting NDVI raster was exported from GEE as a GeoTIFF file and imported into QGIS. In QGIS, the NDVI layer was reprojected, clipped to the study boundary, and further analyzed using raster statistics and classification to evaluate vegetation cover across different spatial units along the Teplica River.
- For more, see the report: <https://github.com/sdgis-edu-tud/report-asa2025-groupc.git>

## 2.3 Instrument- or software-specific information
- QGIS version 3.34 was used for the spatial analysis within the project. 

# 3. FILE OVERVIEW
Are there multiple versions of the dataset? No

## 3.1 File List

"TeplicaSenica_attributes.gpkg": This file contains normalization results of 8 aspects as follow:
- connectivity to ÜSES (spatial system of ecological stability) [B1uses]
- high impact potential and feasibility [B2pot]
- state of vegetation [B3ndvi]
- need for cooling of microclimate [CA1templ]
- potential for water retention [CA2soil]
- potential for community functions [QL1acl]
- potential for central functions [QL2acg]
- need for green space [QL3gr]

## 3.2 Relationship between files
- all 8 aspects are embedded as attributes within the same .gpkg files (sharing the same id).

## 3.3 File formats and naming conventions
### 3.3.1 File formats
- .gpkg – GeoPackage vector and raster format used for storing spatial geometry and attribute tables. Compatible with QGIS and other modern GIS platforms.

### 3.3.2 Naming conventions
The attributes are named by codes corresponding to the workflow described in the report: <https://github.com/sdgis-edu-tud/report-asa2025-groupc.git>. Attributes BXxxx are criteria related to biodiversity, QLXxxx related to quality of life, and CAXxxx related to climate adaptation.

# 4. DATA-SPECIFIC INFORMATION

- Missing data code: NA, NULL
- Not Applicable: N/A

## 4.1 Data

### 4.1.1 aggregated_clean.gpkg
1. Number of variables: 11

2. Number of cases/rows: 600

3. Variable List:

"fid"
- Full name: Feature ID
- Description: Specific ID for each spatial geometry, generated by QGIS automatically.
- Type of variable: Integer
- Unit of measurement: N/A
- Number of missing values: None

"name"
- Full name: N/A
- Description: Type of each spatial geometry, it's either floodplain or biocorridorriver1, which means those areas included in ÚSES biocorridor along the river Teplica.
- Type of variable: text
- Unit of measurement: N/A
- Number of missing values: None

"id_loc_int"
- Full name: N/A
- Description: A backup attribute with unique value for each feature.
- Type of variable: Integer
- Unit of measurement: N/A
- Number of missing values: None

"QL3gr"
- Full name: Quality of Life 3: need for green
- Description: Need for green area in the vicinity of feature (derived from inverse attraction reach from buildings within 500 m buffer to OSM green areas.)
- Type of variable: Decimal Number
- Unit of measurement: N/A
- Number of missing values: None

"QL1acl"
- Full name: Quality of life 1: Angular choice local
- Description: It shows the spatial potential for community functions (derived from Angular choice analysis with radius 500 m.)
- Type of variable: Decimal Number
- Unit of measurement: N/A
- Number of missing values: None

"QL2acg"
- Full name: Quality of life 1: Angular choice global
- Description: It shows the spatial potential for central urban functions (derived from Angular choice analysis with radii 1000 and 2000 m.)
- Type of variable: Decimal Number
- Unit of measurement: N/A
- Number of missing values: None

"B1uses"
- Full name: Biodiversity 1: Connectivity to ÚSES
- Description: It shows the level of connectivity of spatial geometry with USES (spatial system of ecological stability defined by Slovakian law).
- Type of variable: Decimal Number
- Unit of measurement: N/A
- Number of missing values: None

"B2pot"
- Full name: Biodiversity 2: Potential impact and feasibility of intervention
- Description: An estimate of combined impact and feasibility of biodiversity oriented interventions (for more info, see the report).
- Type of variable: Decimal Number
- Unit of measurement: N/A
- Number of missing values: None

"B3ndvi"
- Full name: Biodiversity 3: Normalised NDVI
- Description: Normalization result of NDVI (Normalized Difference Vegetation Index) calculated using Google Earth Engine in each spatial unit.
- Type of variable: Decimal Number
- Unit of measurement: N/A
- Number of missing values: 83

"CA1temp"
- Full name: Climate Adaption 1: Land surface temperature
- Description: Land surface temperature within spatial geometry, calculated with data from Sentinel-2, LANDSAT, and DEM and computed with a [Google Earth Engine script](https://code.earthengine.google.com/ac986028b56a794aefd3ea54e9cb09ba) made by [Ramadhan](https://www.youtube.com/watch?v=3LOMNzBHmjs) on YouTube (2024).
- Type of variable: Decimal Number
- Unit of measurement: N/A
- Number of missing values: 95

"CA2soil"
- Full name: Climate adaptation 2: soil potential
- Description: Water retention ability and permeability indicator in each spatial geometry based on dominant soil type.
- Type of variable: Decimal Number
- Unit of measurement: N/A
- Number of missing values: None

4. Specialised formats or other abbreviations used: None

5. Total file size: 392kb

# 5. SHARING/ACCESS INFORMATION
## 5.1 Licenses/restrictions placed on the data:
The dataset is shared under the Creative Commons Attribution 4.0 International License (CC BY 4.0). Users are free to use, distribute, and build upon the data, provided proper credit is given to the authors.

## 5.2 Links to other resources:
The report describing the research in more detail is available as a GitHub repository: <https://github.com/sdgis-edu-tud/report-asa2025-groupc.git>

### 5.2.1 Links to publications that cite or use the data:
Not available yet (to be updated after publication)

Data was produced in this publicly accessible project: <https://github.com/sdgis-edu-tud/report-asa2025-groupc.git>

### 5.2.2 Links to other publicly accessible locations of the data: 
N/A

### 5.2.3 Links/relationships to ancillary data sets: 
- Sentinel-2 imagery accessed via Google Earth Engine
- LANDSAT imagery accessed via Google Earth Engine
- DEM imagery accessed via Google Earth Engine
- Slovakian ÚSES system <https://www.sazp.sk/zivotne-prostredie/starostlivost-o-krajinu/zelena-infrastruktura/dokumenty-uses-v-sr>
- Atlas of Slovakia (used for soil characteristics) <https://www.enviroportal.sk/atlas-krajiny-sr>

### 5.2.4 Links to publicly accessible scripts for analysis of the dataset:
- Land Surface temperature accessed via [Ramadhan](https://www.youtube.com/watch?v=3LOMNzBHmjs) at <https://code.earthengine.google.com/ac986028b56a794aefd3ea54e9cb09ba>

### 5.2.5 Was data derived from another source?
Yes
- NDVI data derived from Sentinel-2 satellite imagery
- Soil data derived from secondary hydrological data of Slovakia <https://www.enviroportal.sk/atlas-krajiny-sr>
- LST data derived from from Sentinel-2, LANDSAT, and DEM imagery
- Connectivity to ÚSES was based on Slovakian ÚSES system <https://www.sazp.sk/zivotne-prostredie/starostlivost-o-krajinu/zelena-infrastruktura/dokumenty-uses-v-sr>

## 5.3 Recommended citation for this dataset:
Ebermannová, V., Kang, H., Schoonderwoerd, K. (2025). Urban Stream Restoration Dataset of Teplica in Senica, Slovakia [Data set]. Delft University of Technology. https://github.com/sdgis-edu-tud/report-asa2025-groupc

The README.md file template that this file uses was generated on 2022-04-19 by Claudiu Forgaci and Adele Therias according to the 4TU.ResearchData [Guidelines for creating a README file](https://data.4tu.nl/info/en/use/publish-cite/upload-your-data-in-our-data-repository) and the Cornell University template [Guide to writing "readme" style metadata](https://cornell.app.box.com/v/ReadmeTemplate) and is licensed under CC BY 4.0
