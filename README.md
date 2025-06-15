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
  - [4.1 Data Category A](#41-data-category-a)
  - [4.2 Data Category B](#42-data-category-b)
  - [4.3 Data Category C](#43-data-category-c)
  - [4.4 Data Category D](#44-data-category-d)
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
- Address: 
- Email: 

B. Associate or Co-investigator
- Name: Hongyue Kang
- Institution: Technology University of Delft
- Address: Zusterlaan 264b, Delft
- Email: hongyuekang@tudelft.nl

C. Associate or Co-investigator
- Name: Kelly Schoonderwoerd
- Institution: Technology University of Delft
- Address: 
- Email: 

D. Associate or Co-investigator
- Name: Jiaoyang Wu
- Institution: Technology University of Delft
- Address: 
- Email:

## 1.4 Dates of data collection
- NDVI: 2025-05-12
- Survey 2: YYYY-MM-DD

## 1.5 Geographic location of data collection
Senica, Slovakia

## 1.6 Keywords
Sustainable stream restoration, regional ecological stability system, soil, NDVI, land surface temperature, ...

## 1.7 Language
English

# 2. METHODOLOGICAL INFORMATION
## 2.1 Research questions, methods and envisioned uses
The research combines a lot of quantitative GIS-based spatial analysis with qualitative typological classification of street interfaces using Google Street View. This mixed-methods approach enables both a broad spatial overview and a detailed understanding of urban space alongside the Teplica in Senica.

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
3. The resulting NDVI raster was exported from GEE as a GeoTIFF file and imported into QGIS.
4. In QGIS, the NDVI layer was reprojected (if necessary), clipped to the study boundary, and further analyzed using raster statistics and classification to evaluate vegetation cover across different spatial units along the Teplica River.
- ...

## 2.3 Instrument- or software-specific information
- QGIS version 3.34 was used for most of the spatial analysis within the project. 

# 3. FILE OVERVIEW
Are there multiple versions of the dataset? No

## 3.1 File List

### 3.1.1 Data category A
"aggregated_clean.gpkg": This file contains normalization results of 8 aspects as follow:
- connectivity to ÜSES (spatial system of ecological stability) [B1uses]
- high impact potential and feasibility [B2pot], state of vegetation [B3ndvi]
- need for cooling of microclimate [CA1templ]
- potential for water retention [CA2soil]
- potential for community functions [QL1acl]
- potential for central functions [QL2acg]
- need for green space [QL3gr]

## 3.2 Relationship between files
- all 8 aspects are within the same .gpkg files, sharing the same id already.

## 3.3 File formats and naming conventions
### 3.3.1 File formats
- .gpkg – GeoPackage vector and raster format used for storing spatial geometry and attribute tables. Compatible with QGIS and other modern GIS platforms.

### 3.3.2 Naming conventions
N/A(I don't think we need to write sth here)

# 4. DATA-SPECIFIC INFORMATION

- Missing data code: NA
- Not Applicable: N/A

## 4.1 Data Category A

### 4.1.1 aggregated_clean.gpkg
1. Number of variables: 13

2. Number of cases/rows: 600

3. Variable List:

"variable_fid"
- Full name: Feature ID
- Description: Specific ID for each spatial geometry, generated by QGIS automatically.
- Type of variable: Integer
- Unit of measurement: N/A
- Number of missing values: None

"variable_name"
- Full name: N/A
- Description: Type of each spatial geometry, it's either floodplain or biocorridorriver1, which means those areas alongside Teplica.
- Type of variable: text
- Unit of measurement: N/A
- Number of missing values: None

"variable_id_loc_int"
- Full name: ?
- Description: ?
- Type of variable: Integer
- Unit of measurement: N/A
- Number of missing values: None

"variable_QL3gr"
- Full name: Quality of Life3: green
- Description: Priority of need for green area.
- Type of variable: Decimal Number
- Unit of measurement: N/A
- Number of missing values: None

"variable_QL1acl"
- Full name: ?
- Description: It shows the potential for community functions.
- Type of variable: Decimal Number
- Unit of measurement: N/A
- Number of missing values: 327

"variable_QL2acg"
- Full name: ?
- Description: It shows the potential for central functions.
- Type of variable: Decimal Number
- Unit of measurement: N/A
- Number of missing values: 327

"variable_B1uses"
- Full name: ?
- Description: It shows the connectivity of sptial geometry with USES (spatial system of ecological stability).
- Type of variable: Decimal Number
- Unit of measurement: N/A
- Number of missing values: None

"variable_LU_rough"
- Full name: ?
- Description: ?
- Type of variable: text
- Unit of measurement: N/A
- Number of missing values: None

"variable_LU"
- Full name: ?
- Description: ?
- Type of variable: text
- Unit of measurement: N/A
- Number of missing values: None

"variable_B3ndvi"
- Full name: normalization
- Description: normalization result of NDVI in each spatial geometry based on the research question
- Type of variable: Decimal Number
- Unit of measurement: N/A
- Number of missing values: 83

"variable_CA1temp"
- Full name: Climate Adaption temperature corrected
- Description: Land surface temperature within spatial geometry
- Type of variable: Decimal Number
- Unit of measurement: N/A
- Number of missing values: 95

"variable_CA2soil"
- Full name: normalization
- Description: normalization result of water retention potential in each spatial geometry based on the research question.
- Type of variable: Decimal Number
- Unit of measurement: N/A
- Number of missing values: None

4. Specialised formats or other abbreviations used: None

5. Total file size: 428kb

# 5. SHARING/ACCESS INFORMATION
## 5.1 Licenses/restrictions placed on the data:
The dataset is shared under the Creative Commons Attribution 4.0 International License (CC BY 4.0). Users are free to use, distribute, and build upon the data, provided proper credit is given to the authors.

## 5.2 Links to other resources:
?

### 5.2.1 Links to publications that cite or use the data:
Not available yet (to be updated after publication)

### 5.2.2 Links to other publicly accessible locations of the data: 
GitHub repository: https://github.com/sdgis-edu-tud/report-asa2025-groupc

### 5.2.3 Links/relationships to ancillary data sets: 
-Sentinel-2 imagery accessed via Google Earth Engine
-Slovakian landcover
......

### 5.2.4 Links to publicly accessible scripts for analysis of the dataset:
- ?

### 5.2.5 Was data derived from another source?
Yes
-NDVI data derived from Sentinel-2 satellite imagery
-Soil data derived from secondary hydrological data of Slovakia
......

## 5.3 Recommended citation for this dataset:
Ebermannová, V., Kang, H., Schoonderwoerd, K., & Wu, J. (2025). Urban Stream Restoration Dataset of Teplica in Senica, Slovakia [Data set]. Delft University of Technology. https://github.com/sdgis-edu-tud/report-asa2025-groupc

This README.md file template was generated on 2022-04-19 by Claudiu Forgaci and Adele Therias according to the 4TU.ResearchData [Guidelines for creating a README file](https://data.4tu.nl/info/en/use/publish-cite/upload-your-data-in-our-data-repository) and the Cornell University template [Guide to writing "readme" style metadata](https://cornell.app.box.com/v/ReadmeTemplate) and is licensed under CC BY 4.0
