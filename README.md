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
<img width="480" alt="image" src="https://github.com/user-attachments/assets/d96a3732-d4d4-4bd4-9db2-b7fee7220cf6" />

## 6. Insert the Data File ID and Map File ID to merge the data.
#### For example, if you want to merge the two files based on Province, the Province name in the data file is represented by the column "Provinsi" while the Province name in the map file is represented by the column (usually NAME_1).
<img width="480" alt="image" src="https://github.com/user-attachments/assets/12988bbc-6a95-4f1f-8066-43c0a67852c5" />

#### Ensure that the names (in this case, provinces) match those in the map file. If there are discrepancies, adjustments need to be made directly in the Excel file.

## 7. Click Analyze. And then, several summaries will appear
#### Model Summary 
This is the summary of the OLS regression model. In the **Call** section, you can see the syntax of the model. The **Residuals** section shows the distribution of the residuals, which represent the differences between the observed and predicted values for each data point in the model. In the **Coefficients** section, the **Estimate** column provides the coefficient estimates for the intercept and the X variables, forming the general regression model equation. To assess the significance of each parameter, you can check the **Pr(>|t|)** column, also known as the p-value, and compare it to the significance level. If the p-value is smaller than the significance level, the parameter is considered significant in the model, which is also indicated by symbols next to the p-value in the top right corner. 

<img width="480" alt="image" src="https://github.com/user-attachments/assets/a961e79d-8d64-4100-8355-7965f257580d" />

#### Residual Diagnostics
In the **VIF** section, it is used to test for multicollinearity among the predictor variables. If the VIF values for each variable are less than 5 or 10, it indicates that there is no multicollinearity. If a variable's VIF is greater than 10, it can cause unreliable coefficient estimates, leading to inflated standard errors, and thus, the p-values may become misleading. Removing such variables helps to improve model stability, reduce redundancy, and provide more accurate and interpretable results. In the **Normality** section, the normality of residuals must be satisfied. This is determined by checking whether the p-value is greater than the significance level. If the p-value is greater than the significance level, it suggests that the residuals are normally distributed, and the assumption of normality is met. In the **Homoscedasticity** section, if the p-value is greater than the significance level, it indicates that the assumption of homoscedasticity is met. This means that the variance of the residuals is constant across all levels of the independent variables. However, if the p-value is smaller than the significance level, it suggests that the assumption is violated, and the residuals exhibit heteroscedasticity, meaning the variance of the residuals is not constant. In such cases, further steps may be needed, such as applying transformations to the dependent variable, using weighted least squares regression, or employing robust standard errors to correct for heteroscedasticity.

<img width="480" alt="image" src="https://github.com/user-attachments/assets/1c10d76f-6884-4fa7-a3c7-738d60add7fb" />

####  Lagrange Multiplier Test
In the **LM Test** (Lagrange Multiplier Test) for spatial dependence, several parameters are tested to determine whether there is spatial autocorrelation in the model's residuals. 

1. **RSerr (Residuals Error)** tests spatial autocorrelation in the residuals without considering spatial lag effects. If the p-value is greater than the significance level, it indicates no spatial autocorrelation in the residuals.

2. **RSlag (Lag Error)** examines spatial autocorrelation based on the influence of spatial lag, meaning the dependence between residuals at different locations. A p-value smaller than the significance level suggests the presence of spatial autocorrelation, indicating the need for a model that accounts for spatial dependence.

3. **adjRSerr (Adjusted Residuals Error)** is an adjusted version of RSerr, accounting for spatial dependence in the adjusted residuals. If the p-value is greater than the significance level, it indicates no significant spatial dependence in the adjusted residuals.

4. **adjRSlag (Adjusted Lag Error)** is the adjusted version of RSlag, which tests spatial dependence by considering the adjusted residuals with spatial lag effects. A p-value smaller than the significance level suggests the presence of spatial autocorrelation in the adjusted residuals.

5. **SARMA (Spatial Auto-Regressive Model)** tests the overall spatial autocorrelation by considering both spatial dependence in residuals and the influence of spatial lag. If the p-value is slightly smaller than the significance level, it indicates the potential need for a model that accounts for spatial autocorrelation.

Generally, a p-value smaller than the significance level (e.g., 0.05) suggests the presence of spatial dependence that should be addressed in the model. On the other hand, a p-value greater than the significance level indicates that the assumption of no spatial autocorrelation holds, allowing the use of a standard regression model.

<img width="480" alt="image" src="https://github.com/user-attachments/assets/4eb0ee39-02c3-4979-a9e1-a7fc26ac2281" />


####  Morans I Test
The **Moran's I Test under Randomization** is used to examine whether there is spatial autocorrelation in the residuals of the regression model. 

- The **Moran I statistic** indicates the degree of spatial autocorrelation in the residuals. Positive values suggest that similar residuals are spatially clustered, while negative values suggest they are dispersed.

- The **expectation** represents the value of the Moran's I statistic under the null hypothesis of no spatial autocorrelation, which assumes that the residuals are randomly distributed across space.

- The **variance** shows how much the Moran's I statistic is expected to vary under the null hypothesis.

- The **standard deviate** measures how far the observed Moran's I statistic is from its expected value in terms of standard deviations.

- The **p-value** tests whether the observed Moran's I statistic is significantly different from what would be expected under the null hypothesis. A p-value greater than the significance level (e.g., 0.05) suggests no significant spatial autocorrelation in the residuals, while a p-value smaller than the significance level indicates the presence of spatial autocorrelation.

In summary, the Moran's I test helps determine whether spatial patterns are present in the residuals. If the p-value is larger than the significance level, the assumption of no spatial autocorrelation holds, indicating that the residuals do not exhibit spatial dependence.

<img width="480" alt="image" src="https://github.com/user-attachments/assets/2b7ec536-8020-43de-8d37-ea21d3a7a6ef" />

## 8. Choose the best spatial model based on the OLS assumption tests

#### You can see the distribution map of each variable
<img width="480" alt="image" src="https://github.com/user-attachments/assets/ec7eed4f-0dc9-4225-b620-477bd4ea8046" />
<img width="480" alt="image" src="https://github.com/user-attachments/assets/0c9ac0bd-b461-46bf-ae72-e7ef6d484cae" />

#### Best Spatial Model?
In this data case, homoscedasticity assumption is met, the LMLag test is significant, so the Lag model becomes the best model. Additionally, a way to compare one spatial model to another is by finding the model with the lowest AIC value
<img width="480" alt="image" src="https://github.com/user-attachments/assets/74822ddc-ebde-4810-bc62-84ccff4422ab" />




