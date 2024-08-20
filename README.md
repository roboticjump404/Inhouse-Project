# Rice Sales Demand Forecasting

## Project Overview

This project focuses on forecasting rice sales demand at fair price shops in India using various machine learning algorithms. The goal is to predict future Custom Milled Rice (CMR) demand based on historical data from 2018 to 2023.

## Objectives

- **Predict CMR**: Forecast future rice sales demand for the year 2024.
- **Compare Algorithms**: Evaluate the performance of different machine learning models such as XGBoost, CatBoost, SVR, and Random Forest Regressor.
- **Optimize Model**: Fine-tune model parameters to achieve the best prediction accuracy.

## Dataset

- **Source**: The dataset includes monthly demand for Custom Milled Rice (CMR) from January 2018 to December 2023.
- **Features**:
  - `Month`: Represents the month.
  - `CMR`: Custom Milled Rice demand (target variable).
  - `last_1_month` to `last_12_month`: Lag features representing the previous 12 months' CMR.
  - `month`, `quarter`, `year`: Time-related features derived from the `Month` column.

## Preprocessing

1. **Handling Missing Values**: Missing values in lag features are imputed using the median, given the data's almost symmetric distribution with a slight negative skew.
2. **Feature Scaling**: MinMaxScaler is used to scale the data, as it provides a minor error reduction for SVR, though it did not significantly impact other models.

## Model Training

- **Training Period**: The models are trained on data from 2018 to 2022.
- **Testing Period**: The models are tested on the data from 2023.
- **Lag Features**: Twelve lag features are included to improve the models' predictive performance.

## Models Used

1. **XGBoost**
2. **CatBoost**
3. **SVR**
4. **Random Forest Regressor**

## Evaluation Metrics

- **MSE (Mean Squared Error)**
- **RMSE (Root Mean Squared Error)**
- **MAE (Mean Absolute Error)**
- **MAPE (Mean Absolute Percentage Error)**

