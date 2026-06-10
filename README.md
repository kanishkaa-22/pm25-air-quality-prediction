---

## 🚀 How to Run

### 1. Clone the repository
```bash
git clone https://github.com/kanishkaa-22/pm25-air-quality-prediction
cd pm25-air-quality-prediction
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

### 3. Download the dataset
Download from [Kaggle](https://www.kaggle.com/datasets/aravindpcoder/beijing-multi-site-air-quality-data)
and place the CSV in the project folder.

### 4. Train the model
Run `aqi_predection_ml.ipynb` in Google Colab — this will:
- Clean and preprocess the data
- Train all 3 models
- Save the best model as `pm25_rf_model.pkl`

### 5. Upload model to Google Drive
Upload `pm25_rf_model.pkl` to your Google Drive root folder.

### 6. Run the Streamlit app
```bash
streamlit run app.py
```
> Note: Running in Google Colab requires ngrok for public URL access.

---

## 🌐 Deployment

| Component | Detail |
|-----------|--------|
| Model serialized | joblib → pm25_rf_model.pkl |
| Model stored | Google Drive |
| App framework | Streamlit |
| Runtime | Google Colab |
| Public access | ngrok tunnel |

---

## 📈 Key Findings

- **PM10** is the most influential feature — both are fine particulate matter
- **Meteorological features** (TEMP, DEWP, WSPM) significantly affect PM2.5 dispersal
- **Random Forest** outperformed both Linear Regression and XGBoost
- **Linear Regression MAE** is high (118) because PM2.5 has non-linear relationships
- **R² of 0.9312** means the model explains 93% of PM2.5 variance

---

## ⚠️ Limitations

- Model trained on Beijing data — may not generalise to all cities
- SPM feature was unavailable (100% missing in original dataset)
- No real-time sensor data integration
- Meteorological data limited to 12 stations in Beijing

---

## 🔭 Future Scope

- Integrate real-time sensor data feeds
- Include more cities and monitoring stations
- Implement LSTM for time-series PM2.5 forecasting
- Build a mobile app for public AQI alerts
- Add more meteorological features (humidity, solar radiation)

---

## 🏢 Internship Project

This project was developed during an internship.

| | |
|-|-|
| Domain | Data Science / Machine Learning |
| Focus | End-to-end ML pipeline with deployment |
| Organization | TANSAM-Chennai |
| Period | 9 days |

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

<p align="center">
Made with ❤️ | PM2.5 Air Quality Prediction | Beijing Dataset | Random Forest
</p>
