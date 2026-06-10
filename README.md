# 🌫️ PM2.5 Air Quality Prediction Using Machine Learning

> Predicting PM2.5 concentration using regression-based ML models
> trained on the Beijing Multi-Site Air Quality Dataset (2013–2017).

## 📌 Problem Statement

PM2.5 is the most harmful air pollutant — smaller than 2.5 micrometres,
it bypasses the body's filters and enters the lungs and bloodstream,
causing respiratory and cardiovascular diseases.

This project predicts PM2.5 concentration from pollutant and weather
sensor readings using machine learning regression models.

## 📂 Dataset

| Property | Details |
|----------|---------|
| Name | Beijing Multi-Site Air Quality Dataset |
| Period | March 2013 – February 2017 |
| Stations | 12 monitoring stations across Beijing |
| Rows | 420,000+ hourly readings |
| Source | [Kaggle](https://www.kaggle.com/datasets/aravindpcoder/beijing-multi-site-air-quality-data) |

## 🔢 Features Used

| Feature | Type | Description |
|---------|------|-------------|
| PM10 | Pollutant | Particulate matter <= 10 microns (ug/m3) |
| SO2 | Pollutant | Sulphur dioxide (ug/m3) |
| NO2 | Pollutant | Nitrogen dioxide (ug/m3) |
| CO | Pollutant | Carbon monoxide (ug/m3) |
| O3 | Pollutant | Ozone (ug/m3) |
| TEMP | Weather | Temperature (C) |
| PRES | Weather | Atmospheric pressure (hPa) |
| DEWP | Weather | Dew point (C) |
| RAIN | Weather | Rainfall (mm) |
| WSPM | Weather | Wind speed (m/s) |
| **PM2.5** | **Target** | **Fine particulate matter (ug/m3)** |

## ⚙️ Pre-Processing Pipeline

| Step | Action |
|------|--------|
| 1 | Dropped irrelevant columns |
| 2 | Dropped rows where PM2.5 was missing |
| 3 | Imputed missing features using Mean / Median |
| 4 | Outlier capping using IQR Winsorization |
| 5 | Train/Test split — 80% / 20% |

## 🤖 Models Used

| Model | Type |
|-------|------|
| Multiple Linear Regression | Baseline |
| Random Forest Regressor ⭐ | Best Model |
| XGBoost Regressor | Boosting |

## 📊 Results

| Model | MAE | RMSE | R2 Score | Quality |
|-------|-----|------|----------|---------|
| Multiple Linear Regression | 118.1555 | 25.7366 | 0.8572 | Good |
| Random Forest ⭐ | 11.2010 | 17.8647 | **0.9312** | Excellent |
| XGBoost | 12.6010 | 19.2954 | 0.9197 | Excellent |

**Best Model : Random Forest — R2 = 0.9312**

## 🛠️ Tech Stack

| Layer | Tools |
|-------|-------|
| Language | Python |
| Data Processing | Pandas, NumPy |
| Visualization | Matplotlib, Seaborn |
| Machine Learning | scikit-learn, XGBoost |
| Model Saving | joblib |
| Web App | Streamlit |
| Runtime | Google Colab |
| Storage | Google Drive |
| Tunnel | ngrok |

## 🚀 How to Run

1. Download dataset from Kaggle (link above)
2. Run aqi_predection_ml.ipynb in Google Colab
3. Upload pm25_rf_model.pkl to Google Drive
4. Run the Streamlit app:  streamlit run app.py

Note: Google Colab requires ngrok for public URL access.

## 🌐 Deployment

Model serialized using joblib and stored on Google Drive.
Streamlit app runs on Google Colab and is made publicly
accessible via ngrok tunnel.

## 🏢 Internship Project

| | |
|-|-|
| Domain | Data Science / Machine Learning |
| Organization | TANSAM-Chennai |
| Period | 9-days|

<p align="center">Made with ❤️ | PM2.5 Air Quality Prediction | Random Forest | R2 = 0.9312</p>
