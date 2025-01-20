# Predicting Rent Prices Using Machine Learning

This repository contains the project report and implementation files for predicting apartment rent prices in Texas, USA, using machine learning techniques. The project also explores feature importance to identify the most influential factors affecting rent prices.

## Overview

The objective of this project is to predict apartment rent prices and determine the importance of various features, including apartment size, location, and amenities. This value-based pricing approach provides insights into customer-centric factors influencing rental costs.

## Data

- **Source**: UCI Machine Learning Repository (2019)
- **Scope**: Rent data for apartments in Texas, USA
- **Features**: 21 attributes, including apartment type, bedrooms, bathrooms, amenities, and geographic details (latitude, longitude).

## Methodology

### Data Preprocessing
- Filtered dataset to focus on apartments in Texas with rent under $2,000.
- Removed irrelevant columns and transformed categorical variables into binary features.
- Used DBSCAN clustering with Haversine distance to group geographic locations into 11 clusters.

### Models and Validation
- Data split into training (60%), validation (20%), and testing (20%) sets.
- Models implemented:
  - **Linear Regression**: Baseline model for interpretability.
  - **Ridge Regression (L2 regularization)**: To manage multicollinearity.
  - **Lasso Regression (L1 regularization)**: For feature selection.
- Evaluation metrics:
  - Mean Squared Error (MSE)
  - Root Mean Squared Error (RMSE)
  - Mean Absolute Error (MAE)
  - Mean Absolute Percentage Error (MAPE)
  - R-squared (R²)

## Results

- **Best Model**: Linear Regression
  - **R²**: 0.52
  - **MSE (Test)**: $157,768
  - **RMSE (Test)**: $397.2
  - **MAPE**: 0.28%
- **Feature Importance**:
  - Top features: Location clusters, "Elevator," "Luxury," "Alarm," and "Doorman."
  - Geographic location (e.g., Cluster 7 - Odessa/Midland) significantly impacts rent.

## Key Findings

- Location is the most influential factor in predicting rent prices, with 8 out of the top 10 important features being location clusters.
- Linear regression was chosen for its simplicity and comparable performance to Ridge and Lasso regression.

## Limitations and Future Work

- Testing errors indicate potential overfitting; reducing the number of features may improve generalization.
- Incorporating additional features like socioeconomic factors or property-specific details could enhance model performance.
- Future work may explore advanced ML techniques, such as ensembling or neural networks, for better predictive accuracy.

## Repository Contents

- **Data**: Preprocessed datasets for training, validation, and testing.
- **Code**: Python scripts for data preprocessing, model training, and evaluation.
- **Report**: Detailed project report summarizing methodology and findings.

## Authors
This project was completed by a collaborative team as part of a machine learning coursework.

## References
- UCI Machine Learning Repository
- DBSCAN and Haversine distance metrics for clustering
- scikit-learn documentation for regression models
