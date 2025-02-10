# The Impact of Meteorological Parameters on Air Pollution

## Project Overview
This project analyzes the relationship between meteorological parameters and air pollution levels. It implements linear and polynomial regression with feature engineering to predict sulfur dioxide (air pollutant) concentrations.

## Research Hypothesis
Lower temperatures lead to increased sulfur dioxide (SO2) concentrations in the air, while higher wind speeds reduce its levels.

## Dataset Description
The dataset contains hourly measurements from 2013 to 2017, including:
- Air pollutants: PM2.5, PM10, SO2, NO2, CO, O3
- Meteorological parameters: Temperature, Pressure, Dew point, Rain, Wind direction, Wind speed


## Analysis highlights
1. Dew point temperature, unexpectedly, has the most impact on SO2 levels in polynomial models
2. Temperature shows strongest negative correlation with SO2.
3. Polynomial regression with feature engineering achieves $R^2=0.82$
4. Regularization (Lasso, Ridge) does not significantly improve results, since the dataset has a large amount of records and a relativaly small group of features.
5. The significance of meteorological features alone is limited. Models based solely on weather achieved high error values. 
6. Strong correlations between pollutants

## Methods
1. **Data Preprocessing**:
   - KNN imputation for missing values
   - Categorical variable encoding

2. **Feature Engineering**:
   - Temporal feature creation - captured seasonal patterns
   - Log transformations - handling of skewed distributions

3. **Models Implemented**:
   - Linear Regression
   - Polynomial Regression
   - Ridge and Lasso Regularization

4. **Evaluation Metrics**:
   - RMSE
   - $R^2$ Score
   - Mean Absolute Percentage Error (MAPE)
   - Cross-validation scores

## Future improvements
1. Implement more advanced models (Random Forests, XGBoost)
2. Extend analysis to multiple monitoring stations


### Dataset source
[UC Irvine Machine Learning Repository](https://archive.ics.uci.edu/dataset/501/beijing+multi+site+air+quality+data)