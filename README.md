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
<img width="480" alt="image" src="https://github.com/user-attachments/assets/14cdc622-0da8-41b3-b5a5-6e2f0c70e479" />
<img width="480" alt="image" src="https://github.com/user-attachments/assets/9c7cf0c0-9bb9-475c-a91a-37f5ef629dbb" />

## 5. Insert the Y variable (Response Variable) and X variables (Predictor Variables)
#### The Y variable can only be a single variable, while the X variables can include multiple variables.
<img width="480" alt="image" src="https://github.com/user-attachments/assets/817ba445-4e84-4b07-b655-ff4bb0d53b78" />

## 6. Insert the Data File ID and Map File ID to merge the data.
#### For example, if you want to merge the two files based on Province, the Province name in the data file is represented by the column "Provinsi" while the Province name in the map file is represented by the column (usually NAME_1).
<img width="480" alt="image" src="https://github.com/user-attachments/assets/512281f9-9dd4-47ef-9b95-541a4203fc16" />

#### Ensure that the names (in this case, provinces) match those in the map file. If there are discrepancies, adjustments need to be made directly in the Excel file.

## 7. Click Analyze. And then, several summaries will appear.
#### Model Summary 
Ini Merupakan 
<img width="960" alt="image" src="https://github.com/user-attachments/assets/2e459d0e-a974-4d74-8aa7-9669649b0f93" />


