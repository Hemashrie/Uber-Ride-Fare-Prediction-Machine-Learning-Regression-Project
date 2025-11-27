## Uber Ride Fare Prediction – Regression Analysis Project

## Project Summary

This project focuses on building a Regression Machine Learning Model to predict the fare amount of Uber rides based on trip details such as pickup/dropoff coordinates, distance, time, and passenger count.
The goal is to develop an end-to-end ML pipeline that includes data preprocessing, feature engineering, model training, evaluation, and hyperparameter tuning, ensuring accurate and reliable fare predictions.

 ## Project Overview

Uber provides a large volume of ride-related data.

## This project aims to:

- Understand the relationship between ride attributes and fare amount.
- Engineer meaningful features (distance, time-of-day, etc.)
- Compare multiple regression models.
- Optimize model performance using hyperparameter tuning.
- Generate insights that help improve pricing strategies.

## Files in This Repository

- File Name	Description
- uber.csv	Raw dataset containing Uber ride information.
- Predict_Ride_Fare_Amount_RegressionAnalysis.ipynb	Complete end-to-end model pipeline: cleaning, EDA, modeling, tuning, and insights.
  
## Tools & Libraries Used

## Python:

- Pandas – Data cleaning & preprocessing
- NumPy – Numerical operations
- Matplotlib / Seaborn – Data visualization
- Scikit-Learn – Machine Learning models & evaluation
- Jupyter Notebook – Development environment

## Key Steps Performed

## Data Cleaning:

- Removed missing and invalid values
- Corrected datatypes
- Cleaned inconsistent coordinates and passenger counts
- Feature Engineering:
- Converted datetime into year/month/day/hour
- Extracted time-of-day categories
- Calculated distance using the Haversine formula

## Exploratory Data Analysis (EDA):

- Distribution of fares
- Distance vs. fare relationship
- Passenger count patterns
- Heatmaps and correlation analysis

## Model Building:

- Linear Regression
- Decision Tree Regressor
- Random Forest Regressor
- Hyperparameter Tuning:
- Used RandomizedSearchCV for fast tuning

Optimized parameters: n_estimators, max_depth, splits

## Model Evaluation:

- MAE (Mean Absolute Error)
- RMSE (Root Mean Squared Error)
- R² Score

## Predictions:

- Predicting fare for new ride inputs
- Ensuring feature order matches trained model inputs

 ## Insights Discovered 

- Trip distance is the strongest predictor of fare amount.
- Time-of-day and hour influence pricing moderately.
- Passenger count has minimal impact except in extreme cases.
- Tuned Random Forest achieved the best prediction performance.

 ## How to Use

- Download or clone this repository.
- Open the .ipynb file in Jupyter Notebook or VS Code.
- Run all cells to reproduce preprocessing, EDA, model training, and predictions.
- Modify input values in the prediction section to test new ride fares.

Example prediction snippet:

new_df = new_df[X_train.columns]   # Match training column order
best_rf.predict(new_df)

## Author

Created by: Hema Shrie

Email: rhemashrie156@gmail.com





