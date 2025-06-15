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
This dataset contains quantitative data on normalization of 8 different MCDA aspects based on spatial geometry alongside stream Teplica, to answer the question where should be prioritized for stream restoration. Additional details about the project can be accessed [here](https://github.com/sdgis-edu-tud/report-asa2025-groupc).

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
- "B1 use.gpkg": brief description of file

### 3.1.2 Data category B
- "B2 pot.gpkg": brief description of file

### 3.1.3 Data category C
- "B3 NDVI.gpkg": This file contains normalization result of NDVI within the geometry alongside the Teplica, which is based on our research question: Which spaces should be prioritized based on current state of vegetation?

### 3.1.4 Data category D
- "CA1 temp.gpkg": brief description of file

### 3.1.5 Data category E
- "CA2 soil.gpkg": This file shows the soil retention ability and permeability map, as well as normalization result within the spatial geometry based on the research question: Where is potential for water retention? 

## 3.2 Relationship between files:??????????????????????????
(The following tables (csv files) employ a foreign key to refer to the primary key (unique identifier) in one or more other table(s):

"filename.extension"
- abc used as foreign key to "otherfile.extension")----this part I can not understand
- These GeoPackage files represent different thematic datasets for the same spatial units. Although they share identical spatial boundaries, their attribute tables contain unrelated fields. There is no direct key-based linkage between the datasets; their relationship is spatial rather than relational.

## 3.3 File formats and naming conventions
### 3.3.1 File formats
- .gpkg – GeoPackage vector and raster format used for storing spatial geometry and attribute tables. Compatible with QGIS and other modern GIS platforms.

### 3.3.2 Naming conventions
- Prefixes like B1, B2, CA1, CA2 indicate thematic category and sequence, for instance, B represnents for Biodiversity, and CA is for Climate Adaption.
- Suffixs means different factors reflecting the themes.
- Prefix is in Uppercase, suffix is in lowercase.

# 4. DATA-SPECIFIC INFORMATION

- Missing data code: NA
- Not Applicable: N/A

## 4.1 Data Category A

### 4.1.1 B1 use.gpkg
1. Number of variables: 6

2. Number of cases/rows: 600

3. Variable List:

"variable_fid"
- Full name: Feature ID
- Description: Specific ID for each spatial geometry, generated by QGIS automatically.
- Type of variable: Integer
- Unit of measurement: N/A
- Number of missing values: None

"variable_id_loc_int"
- Full name: ?
- Description: ?
- Type of variable: Integer
- Unit of measurement: N/A
- Number of missing values: None

"variable_QL3gr"
- Full name: ?
- Description: ?
- Type of variable: Decimal Number
- Unit of measurement: N/A
- Number of missing values: None

"variable_QL1acl"
- Full name: ?
- Description: ?
- Type of variable: Decimal Number
- Unit of measurement: N/A
- Number of missing values: 327

"variable_QL2acg"
- Full name: ?
- Description: ?
- Type of variable: Decimal Number
- Unit of measurement: N/A
- Number of missing values: 327

"variable_B1uses"
- Full name: ?
- Description: ?
- Type of variable: Decimal Number
- Unit of measurement: N/A
- Number of missing values: None

4. Specialised formats or other abbreviations used: None

5. Total file size: 352kb

## 4.2 Data Category B

### 4.2.1 B2 pot.gpkg
1. Number of variables: 9

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
- Description: ?
- Type of variable: Integer
- Unit of measurement: N/A
- Number of missing values: None

"variable_code"
- Full name: N/A
- Description: ?
- Type of variable: Integer
- Unit of measurement: N/A
- Number of missing values: None

"variable_id_loc"
- Full name: N/A
- Description: ?
- Type of variable: Integer
- Unit of measurement: N/A
- Number of missing values: None

"variable_id_loc_int"
- Full name: N/A
- Description: ?
- Type of variable: Integer
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

"variable_simplified new"
- Full name: ?
- Description: ?
- Type of variable: Boolean
- Unit of measurement: N/A
- Number of missing values: None

"variable_B2pot"
- Full name: ?
- Description: ?
- Type of variable: Decimal Number
- Unit of measurement: N/A
- Number of missing values: None

4. Specialised formats or other abbreviations used: None

5. Total file size: 368kb

## 4.3 Data Category C

### 4.3.1 B3 ndvi.gpkg
1. Number of variables: 9

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
- Description: ?
- Type of variable: Integer
- Unit of measurement: N/A
- Number of missing values: None

"variable_code"
- Full name: N/A
- Description: ?
- Type of variable: Integer
- Unit of measurement: N/A
- Number of missing values: None

"variable_id_loc"
- Full name: N/A
- Description: ?
- Type of variable: Integer
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

"variable_simplified new"
- Full name: ?
- Description: ?
- Type of variable: Boolean
- Unit of measurement: N/A
- Number of missing values: None

"variable_mean"
- Full name: N/A
- Description: mean of NDVI in each spatial geometry
- Type of variable: Decimal Number
- Unit of measurement: N/A
- Number of missing values: 83

"variable_norm"
- Full name: normalization
- Description: normalization result of NDVI in each spatial geometry based on the research question
- Type of variable: Decimal Number
- Unit of measurement: N/A
- Number of missing values: None

4. Specialised formats or other abbreviations used: None

5. Total file size: 392kb

## 4.4 Data Category D

### 4.4.1 CA1 temp.gpkg
1. Number of variables: 3

2. Number of cases/rows: 599

3. Variable List:

"variable_fid"
- Full name: Feature ID
- Description: Specific ID for each spatial geometry, generated by QGIS automatically.
- Type of variable: Integer
- Unit of measurement: N/A
- Number of missing values: None

"variable_id_loc_int"
- Full name: ?
- Description: ?
- Type of variable: Integer
- Unit of measurement: N/A
- Number of missing values: None

"variable_CA1temp_corrected"
- Full name: Climate Adaption temperature corrected
- Description: Land surface temperature within spatial geometry
- Type of variable: Decimal Number
- Unit of measurement: N/A
- Number of missing values: 95

4. Specialised formats or other abbreviations used: None

5. Total file size: 344kb

## 4.5 Data Category E

### 4.5.1 CA2 soil.gpkg
1. Number of variables: 8

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
- Description: ?
- Type of variable: Integer
- Unit of measurement: N/A
- Number of missing values: None

"variable_code"
- Full name: N/A
- Description: ?
- Type of variable: Integer
- Unit of measurement: N/A
- Number of missing values: None

"variable_id_loc"
- Full name: N/A
- Description: ?
- Type of variable: Integer
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

"variable_simplified new"
- Full name: ?
- Description: ?
- Type of variable: Boolean
- Unit of measurement: N/A
- Number of missing values: None

"variable_norm"
- Full name: normalization
- Description: normalization result of water retention potential in each spatial geometry based on the research question.
- Type of variable: Decimal Number
- Unit of measurement: N/A
- Number of missing values: None

4. Specialised formats or other abbreviations used: None

5. Total file size: 388kb
   
# 5. SHARING/ACCESS INFORMATION
## 5.1 Licenses/restrictions placed on the data:
The dataset is shared under the Creative Commons Attribution 4.0 International License (CC BY 4.0). Users are free to use, distribute, and build upon the data, provided proper credit is given to the authors.

## 5.2 Links to other resources:


### 5.2.1 Links to publications that cite or use the data:
Not available yet (to be updated after publication)

### 5.2.2 Links to other publicly accessible locations of the data: 
GitHub repository: https://github.com/sdgis-edu-tud/report-asa2025-groupc

### 5.2.3 Links/relationships to ancillary data sets: 
-Sentinel-2 imagery accessed via Google Earth Engine
-Slovakian landcover
......

### 5.2.4 Links to publicly accessible scripts for analysis of the dataset:
- ???????????????????????????????

### 5.2.5 Was data derived from another source?
Yes
-NDVI data derived from Sentinel-2 satellite imagery
-Soil data derived from secondary hydrological data of Slovakia
......

## 5.3 Recommended citation for this dataset:
Ebermannová, V., Kang, H., Schoonderwoerd, K., & Wu, J. (2025). Urban Stream Restoration Dataset of Teplica in Senica, Slovakia [Data set]. Delft University of Technology. https://github.com/sdgis-edu-tud/report-asa2025-groupc

This README.md file template was generated on 2022-04-19 by Claudiu Forgaci and Adele Therias according to the 4TU.ResearchData [Guidelines for creating a README file](https://data.4tu.nl/info/en/use/publish-cite/upload-your-data-in-our-data-repository) and the Cornell University template [Guide to writing "readme" style metadata](https://cornell.app.box.com/v/ReadmeTemplate) and is licensed under CC BY 4.0
