# 🔌 Power Consumption Prediction – Zone 1, Wellington

This machine learning project predicts electricity consumption in **Zone 1 of Wellington** using weather and environmental data. It applies data preprocessing, feature engineering, and model tuning to build an effective regression model.

---

## 📁 Project Overview

- **Goal:** Predict power consumption using variables like temperature, humidity, and wind speed.
- **Target Variable:** `Power Consumption in A Zone`
- **Dataset Size:** ~52,000 records
- **Tools Used:** Python, Pandas, Scikit-learn, Matplotlib, Seaborn

---

## 🔧 Workflow Summary

1. **Data Cleaning**
   - Removed missing and non-numeric values
   - Standardized column names

2. **EDA & Preprocessing**
   - Visualized distribution of features
   - Handled skewness using log transformation
   - Detected and removed outliers using IQR method

3. **Feature Engineering**
   - Created interaction features (e.g., `Temperature × Wind Speed`)
   - Applied polynomial feature combinations (degree 2)
   - Dropped highly correlated or redundant features

4. **Model Building**
   - Compared Linear Regression, Random Forest, and XGBoost
   - Performed hyperparameter tuning using GridSearchCV
   - Final model: **Tuned Random Forest Regressor**

---

## 📊 Model Performance

| Model                | R² Score | RMSE     | MAE      |
|----------------------|----------|----------|----------|
| Linear Regression    | ~0.32    | High     | High     |
| XGBoost Regressor    | ~0.55    | Medium   | Medium   |
| **Random Forest (Best)** | **~0.65** | **Low**    | **Low**    |

---

## 📈 Key Features Used

- Temperature
- Humidity
- Wind Speed
- General Diffuse Flows (log-transformed)
- Interaction terms (e.g., `temp × humidity`)
- Polynomial interactions

---

## ✅ Results & Takeaways

- **Random Forest** outperformed other models after feature engineering and tuning.
- Log transformation of skewed variables improved prediction accuracy.
- Adding polynomial and interaction features helped capture non-linear patterns.

---

## 🚀 Future Improvements

- Add time-based features (hour, weekday, season)
- Use LSTM or deep learning for time series forecasting
- Apply SHAP or feature importance analysis for model explainability

---

## 📂 Files Included

- `Project_wellington.ipynb` – Final notebook with complete pipeline
- `City Power Consumption.xlsx` – Original dataset

