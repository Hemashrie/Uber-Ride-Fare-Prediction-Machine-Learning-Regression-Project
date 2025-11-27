Project Overview

The goal of this project is to build a predictive model that estimates the fare amount for Uber rides based on trip features such as pickup/dropoff coordinates, distance, time, and passenger count.

- This end-to-end ML pipeline includes:
  
- Data cleaning & wrangling
- Handling missing values
- Time-based feature engineering
- Distance calculation using Haversine Formula
- Outlier removal
- Train–test split
- Linear Regression, Decision Tree, Random Forest
- Fast Hyperparameter Tuning
- Final model evaluation & insights

 Dataset Information

The dataset contains historical Uber trip details with the following key columns:

- pickup_datetime – Date & time of ride
- pickup_latitude, pickup_longitude
- dropoff_latitude, dropoff_longitude
- passenger_count
- fare_amount (Target variable)
- Additional engineered features:
- Year, Month, Day, Hour
- Weekday
- Time of Day (Morning/Afternoon/Evening/Night)
- Distance (Haversine)

Technologies Used

- Python
- Pandas & NumPy
- Matplotlib & Seaborn
- Scikit-Learn
- Jupyter Notebook

 Data Preprocessing Steps:
 Missing value handling:

Dropped invalid or missing rows.

 Datetime conversion:

Extracted:

- Year
- Month
- Day
- Hour
- Weekday
- Time-of-day category

 Distance calculation:

Computed trip distance using Haversine formula.

 Outlier removal:

Filtered:

- Negative / unrealistic fares
- Distance > 50 km
- Passenger count outside 1–6
- Categorical encoding
- One-hot encoded time_of_day.
  
 Final cleanup:

Dropped pickup_datetime after extracting useful info.

Models Implemented

1️. Linear Regression
Baseline model using scaled numeric features.

2️. Decision Tree Regressor
Captures non-linear relationships.

3️. Random Forest Regressor
Best performing ensemble model.

4️. Hyperparameter Tuned Random Forest
Fast RandomizedSearchCV with optimized parameters.

 Model Evaluation Metrics

Evaluation includes:

- MAE: Mean Absolute Error
- RMSE: Root Mean Squared Error
- R² Score
- The Tuned Random Forest provides the best performance.

 Key Feature Insights

Based on feature importance from Random Forest:

- Distance is the strongest predictor of fare
- Time-based features also influence pricing
- Latitude/Longitude help determine accurate trip length
- Passenger count has minor impact

 Sample Prediction

Sample code for predicting a new ride:

new_df = new_df[X_train.columns]    # Match training column order
best_rf.predict(new_df)


You can replace latitude, longitude, and passenger count with desired inputs.

Repository Structure
├── uber_fare_prediction.ipynb     # Final notebook
├── uber.csv                       # Dataset (if allowed)
├── README.md                      # Project documentation
└── images/                        # Plots (optional)

 Final Results

This project successfully builds an end-to-end ML pipeline that:

- Cleans and prepares raw Uber data
- Creates meaningful features
- Trains multiple regression models
- Tunes and selects the best model
- Produces reliable fare predictions

⭐ Author

Created by: Hema Shrie

Email: rhemashrie156@gmail.com
