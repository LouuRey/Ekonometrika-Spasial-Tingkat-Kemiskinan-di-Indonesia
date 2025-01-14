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
This is the summary of the OLS regression model. In the **Call** section, you can see the syntax of the model. The **Residuals** section shows the distribution of the residuals, which represent the differences between the observed and predicted values for each data point in the model. In the **Coefficients** section, the **Estimate** column provides the coefficient estimates for the intercept and the X variables, forming the general regression model equation. To assess the significance of each parameter, you can check the **Pr(>|t|)** column, also known as the p-value, and compare it to the significance level. If the p-value is smaller than the significance level, the parameter is considered significant in the model, which is also indicated by symbols next to the p-value in the top right corner. 

<img width="480" alt="image" src="https://github.com/user-attachments/assets/2e459d0e-a974-4d74-8aa7-9669649b0f93" />

#### Residual Diagnostics
In the VIF section, it is used to test for multicollinearity among the predictor variables. If the VIF values for each variable are less than 5 or 10, it indicates that there is no multicollinearity. If a variable's VIF is greater than 10, it can cause unreliable coefficient estimates, leading to inflated standard errors, and thus, the p-values may become misleading. Removing such variables helps to improve model stability, reduce redundancy, and provide more accurate and interpretable results.

<img width="480" alt="image" src="https://github.com/user-attachments/assets/99cef9c3-5ada-43b4-8f0b-5646f50373a9" />

#### 

<img width="48" alt="image" src="https://github.com/user-attachments/assets/90957508-902b-42b4-a601-c0e52f75d87b" />

<img width="480" alt="image" src="https://github.com/user-attachments/assets/c2e14e8f-b88e-48c0-8074-a5c6345bf175" />


