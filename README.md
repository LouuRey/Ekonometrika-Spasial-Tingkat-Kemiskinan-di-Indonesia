# Web-Dashboard-Spatial-Analysis-with-R-Shiny

## 1. Prepare the map file, which can be in JSON format, RDS format, or SHP (Zip) format
  - [Example Map File](https://github.com/LouuRey/Web-Dashboard-Spatial-Analysis-with-R-Shiny/blob/main/gadm41_IDN_1.json)

## 2. Prepare the data file, which can be in CSV format or XLSX format.
  - [Example Data File](https://github.com/LouuRey/Web-Dashboard-Spatial-Analysis-with-R-Shiny/blob/main/dataku.xlsx)

## 3. Open the website
  - [Spatial Analysis](https://spatialanalysis.netlify.app/)

## 4. Input the files
<img width="480" alt="image" src="https://github.com/user-attachments/assets/c6faedc8-831a-4505-b4d0-da1a43046bc7" />


#### You can preview the map and the data (Like this)
<img width="907" alt="image" src="https://github.com/user-attachments/assets/5c152d80-f96c-4c6a-ab67-3a9ca41c6eb0" />
<img width="924" alt="image" src="https://github.com/user-attachments/assets/29e76a98-2d24-4f87-b1a7-f0027a9f53dc" />

## 5. Insert the Y variable (Response Variable) and X variables (Predictor Variables)
#### The Y variable can only be a single variable, while the X variables can include multiple variables.
<img width="285" alt="image" src="https://github.com/user-attachments/assets/67fec287-5dcb-483c-9e5b-c479fa2981c0" />

## 6. Insert the Data File ID and Map File ID to merge the data.
#### For example, if you want to merge the two files based on Province, the Province name in the data file is represented by the column "Provinsi" while the Province name in the map file is represented by the column (usually NAME_1).

#### Ensure that the names (in this case, provinces) match those in the map file. If there are discrepancies, adjustments need to be made directly in the Excel file.

