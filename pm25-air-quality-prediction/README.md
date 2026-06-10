# 🌫️ PM2.5 Air Quality Prediction Using Machine Learning

## Problem Statement
Predict PM2.5 concentration from air pollutant and weather readings
using machine learning regression models.

## Dataset
Beijing Multi-Site Air Quality Dataset (2013–2017)
Source: https://www.kaggle.com/datasets/aravindpcoder/beijing-multi-site-air-quality-data

## Features Used
| Feature | Description |
|---------|-------------|
| PM10    | Particulate matter ≤ 10 microns |
| SO2     | Sulphur dioxide |
| NO2     | Nitrogen dioxide |
| CO      | Carbon monoxide |
| O3      | Ozone |
| TEMP    | Temperature (°C) |
| PRES    | Atmospheric pressure (hPa) |
| DEWP    | Dew point (°C) |
| RAIN    | Rainfall (mm) |
| WSPM    | Wind speed (m/s) |

## Target Variable
PM2.5 concentration (µg/m³)

## Models Used
- Multiple Linear Regression (baseline)
- Random Forest Regressor ⭐ Best Model
- XGBoost Regressor

## Tech Stack
- Python, Pandas, NumPy
- Matplotlib, Seaborn
- scikit-learn, XGBoost
- Streamlit (web app)
- Google Colab + ngrok
- joblib (model serialization)

## How to Run
1. Download the dataset from Kaggle
2. Run AQI_Prediction.ipynb to train the model
3. Save the model as pm25_rf_model.pkl
4. Run app.py with streamlit:
streamlit run app.py

## Results
| Model | R² Score |
|-------|----------|
| Linear Regression | 0.xx |
| Random Forest     | 0.xx |
| XGBoost           | 0.xx |