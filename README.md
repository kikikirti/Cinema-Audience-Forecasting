# 🎬 Cinema Audience Forecasting  
**MLP Project T32025 – Kaggle**

## 📌 Project Overview
This project focuses on predicting the **daily audience count** for cinema theaters using historical visit data, booking information, theater metadata, and calendar features. The task is modeled as a **time-series regression problem**.

## 🎯 Objective
Predict `audience_count` for each `book_theater_id` on a given day to support demand forecasting and planning.

## 📂 Datasets Used
- `booknow_visits` – target audience data  
- `booknow_booking` – online bookings  
- `cinePOS_booking` – POS ticket sales  
- `booknow_theaters` & `cinePOS_theaters` – theater metadata  
- `date_info` – calendar features  
- `movie_theater_id_relation` – theater ID mapping  

## 🔍 Approach
1. Data loading and cleaning  
2. Exploratory Data Analysis (EDA)  
3. Missing value handling and outlier treatment  
4. Feature engineering:
   - Date features (day, month, weekend, etc.)
   - Booking aggregates
   - Time-series lag features (`lag1`, `lag7`, `lag7_mean`)
5. Preprocessing using **Pipeline + ColumnTransformer**
6. Model training and comparison

## 🤖 Models Trained
- Ridge Regression (with hyperparameter tuning)
- Random Forest Regressor
- LightGBM Regressor

**Final Model:** Random Forest (chosen based on validation and Kaggle leaderboard performance)

## 📈 Evaluation Metric
- **R² Score**

## 🏆 Results
- Validation R² ≈ **0.55**
- Kaggle Public Leaderboard score **> 0.30**

## 🧠 Key Learnings
- Strong weekend and weekly seasonality in audience data  
- Lag features significantly improve performance  
- Tree-based models outperform linear models for this task  

## 🛠️ Tech Stack
- Python  
- Pandas, NumPy  
- Scikit-learn  
- LightGBM  
- Matplotlib, Seaborn  

## 📁 File
- `notebook.ipynb` – complete end-to-end implementation


