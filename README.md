# House Price Prediction Project

## Overview
This project implements a machine learning pipeline for predicting house prices using various regression techniques. The solution includes data preprocessing, feature engineering, and model training with hyperparameter tuning.

## Features
- Data loading and preprocessing
- Feature engineering with new calculated features
- Multiple regression models with hyperparameter tuning
- Comprehensive model evaluation metrics
- Log-transformed target variable for better performance
- 
## Data Preparation
The script performs the following preprocessing steps:
- Drops unnecessary columns (ID)
- Encodes categorical variables (Location, Condition, Garage)
- Handles missing values by replacing with median
- Creates new features:
  - TotalArea (combining area with bedroom/bathroom space estimates)
  - RoomRatio (bedroom to bathroom ratio)
  - PricePerSqFt (price per square foot)

## Models Implemented
The following regression models are implemented and tuned:

1. **Linear Regression**
   - StandardScaler preprocessing
   - Tuned parameters: fit_intercept, positive

2. **Ridge Regression**
   - StandardScaler preprocessing
   - Tuned parameters: alpha, solver

3. **Decision Tree**
   - Tuned parameters: max_depth, min_samples_split, min_samples_leaf, max_features

4. **Random Forest**
   - Tuned parameters: n_estimators, max_depth, min_samples_split, min_samples_leaf, max_features

## Evaluation Metrics
Each model is evaluated using:
- Root Mean Squared Error (RMSE)
- R-squared (R2) score
- 5-fold cross-validation RMSE

## Results Interpretation
The script outputs:
- Best parameters for each model
- Test set RMSE and R2 scores
- Cross-validation RMSE for stability assessment

## Requirements
- Python 3.6+
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
