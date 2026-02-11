# Bike_Rental_demand-prediction
Machine learning project predicting bike rental demand using Regression model XGBoost with pipelines, cross-validation, and model comparison.
##  Project Overview
This project predicts bike rental demand using machine learning regression models. The goal is to analyze how weather, seasonal, and temporal features affect bike usage and build a model that accurately forecasts rental counts.

The project includes end-to-end implementation: data preprocessing, feature engineering, model comparison, hyperparameter tuning, and feature importance analysis.


##  Problem Statement
Given historical bike rental data, predict the total number of bikes rented (`cnt`) based on:
- Weather conditions
- Season and month
- Working day / holiday
- Hour of the day (for hourly dataset)

This is a **supervised regression problem**.


##  Dataset
Link: https://d3ilbtxij3aepc.cloudfront.net/projects/CDS-Capstone-Projects/PRCP-1018-BikeRental.zip
- Two datasets used:
  - Hourly dataset
  - Daily dataset
- Target variable: `cnt` (total bike rentals)
- Dataset has both categoricl and numerical features

##  Approach

###  Data Preprocessing
- Separated numerical and categorical features
- Applied Standard Scaling to numerical features
- Applied One-Hot Encoding to categorical features
- Used `ColumnTransformer` and `Pipeline` to prevent data leakage

###  Models Implemented
- Linear Regression
- Random Forest Regressor
- Gradient Boosting Regressor
- Support Vector Regressor (SVR)
- KNN Regressor
- XGBoost Regressor (Final Model)

###  Model Evaluation
Models were evaluated using:
- MAE (Mean Absolute Error)
- RMSE (Root Mean Squared Error)
- R² Score
- K-Fold Cross-Validation

XGBoost achieved the best performance on the hourly dataset.

##  Feature Importance
To understand the key drivers of bike demand, highlighting the impact of:
- Hour of the day
- Working day
- Season
- Weather conditions

