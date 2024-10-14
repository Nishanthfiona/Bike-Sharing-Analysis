# Bike Sharing Demand Analysis

## Project Overview
This project analyzes factors affecting the demand for bike-sharing services using Multiple Linear Regression. The aim is to provide insights into key drivers of demand and build a predictive model to help optimize bike availability.

## Dataset
The dataset includes the following key features:
- **Date and Time**: Timestamp of each bike rental.
- **Weather**: Temperature, humidity, wind speed, etc.
- **Season and Holidays**: Information on seasonality, holidays, and working days.
- **Target Variable**: Bike rental demand.

## Steps Involved

### 1. Data Cleaning and Preprocessing
- Removed any missing values and handled outliers.
- Created new time-based features (e.g., hour, weekday).
- Normalized the numerical variables where necessary.

### 2. Exploratory Data Analysis (EDA)
- Visualized relationships between the target variable (bike demand) and features like weather, season, and time of day.
- Identified patterns: higher demand during favorable weather and rush hours.
  
### 3. Feature Selection
- Performed **Recursive Feature Elimination (RFE)** to select key features influencing demand.
- The most important features included: 
  - Temperature
  - Hour of the day
  - Humidity
  - Working day status
  - Windspeed
  
### 4. Model Development
Built a **Multiple Linear Regression** model after validating the following assumptions:
- **Linearity**: The relationship between the predictors and the target is linear.
- **Multicollinearity**: Checked using Variance Inflation Factor (VIF); no significant multicollinearity found.
- **Normality of errors**: Residuals followed a normal distribution.
- **Homoscedasticity**: Constant variance observed in residuals.
- **Independence of errors**: The Durbin-Watson test indicated no autocorrelation.

### 5. Model Evaluation
- The model achieved a high **R-squared value**, explaining a significant proportion of the variance in bike demand.
- All features had low p-values, indicating their statistical significance.
- Cross-validation confirmed the model's robustness.

### 6. Final Model Features
The final model included:
- Temperature
- Hour of the day
- Day of the week
- Working day status
- Humidity
- Windspeed

These features had the most significant impact on predicting bike demand.

## Results
- The model identified key drivers of bike-sharing demand with high accuracy.
- High R-squared and low p-values for features indicate a strong and reliable model.
- The analysis helps the company improve bike demand forecasting and resource management.

## Assumptions Validation
- **Normality of Errors**: Verified using residual plots.
- **Multicollinearity**: Controlled by VIF values.
- **Linearity**: Scatterplots indicated linear relationships between predictors and target.
- **Homoscedasticity**: No patterns observed in residual plots.
- **Independence of Errors**: Durbin-Watson statistic confirmed no autocorrelation.

## Dependencies
- **Python 3.x**
- **Libraries**: 
  - `pandas`
  - `numpy`
  - `matplotlib`
  - `seaborn`
  - `sklearn`
  - `statsmodels`

