# AAPL Price Movement Prediction

A lightweight machine learning project predicting next-day Apple (`AAPL`) stock price direction (Up/Down) using rolling returns and volatility features.

## 📁 Project Structure
* `stock_prediction.ipynb` - Data processing, feature engineering, and model training.
* `README.md` - Project documentation.

## 🛠️ Features & Target
* **Features:** `Return_5`, `Return_10`, `Return_20` & `Vol_5`, `Vol_10`, `Vol_20` (rolling standard deviation).
* **Target (`Signal`):** `1` if tomorrow's price goes up, `0` otherwise.
* **Data Split:** Chronological 80% train (2084 days), 20% validation (521 days).

## 📊 Results

### 1. Logistic Regression (Baseline)
* **Accuracy:** `55.66%`
* **Confusion Matrix:**
```text
    [[  0 231]
    [  0 290]]
```
### 2. Random Forest Classifier (n_estimators=500)
* **Accuracy:** `52.78%`
* **Classification Report:**
  Final Random Forest Accuracy: 0.527831094049904
Classification Report:
```text
               precision    recall  f1-score   support

           0       0.46      0.39      0.43       231
           1       0.57      0.63      0.60       290

    accuracy                           0.53       521
   macro avg       0.51      0.51      0.51       521
weighted avg       0.52      0.53      0.52       521
```
