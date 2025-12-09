

# Stock Price Movement Prediction using Logistic Regression, SVM, and XGBoost

A machine learning project that predicts whether the **next day’s stock price** of **Asian Paints (ASIANPAINT.NS)** will **increase or decrease**.
The model uses **25 years of historical data**, technical indicators, engineered features, and three ML algorithms:

* Logistic Regression
* Support Vector Machine (SVM – RBF Kernel)
* XGBoost Classifier

Each model is evaluated using complete performance metrics, including **Accuracy, Precision, Recall, F1-Score, ROC-AUC**, and **Confusion Matrix**.

---

## **Project Overview**

Stock price direction prediction is a binary classification task where the goal is to determine whether the next day's closing price will go **UP (1)** or **DOWN (0)**.
This project uses:

* YFinance API for historical stock price data
* Technical Indicators for feature engineering
* Machine learning models to predict direction
* Evaluation metrics for comprehensive model assessment

---

## **Features of This Project**

### **1. Technical Indicators Included**

The following indicators are used:

* RSI (Relative Strength Index)
* MACD + Signal Line
* Bollinger Bands (Upper, Lower, Width)
* ATR (Average True Range)
* Return Lags (1-day, 3-day, 5-day)
* Moving Average (MA20)

### **2. ML Algorithms**

* Logistic Regression (baseline linear classifier)
* SVM (RBF kernel for nonlinear separation)
* XGBoost (gradient boosting decision trees)

### **3. Performance Metrics**

Each model prints:

* Accuracy
* Precision
* Recall
* F1 Score
* ROC-AUC
* Confusion Matrix
* Classification Report

### **4. Final Prediction**

The code prints whether the **next day's price will go UP or DOWN** using each model.

---

## **Installation**

### **1. Clone the repository**

```bash
git clone https://github.com/<praveen-ctrl>/<praveen-ctrl>.git
cd <praveen-ctrl>
```

### **2. Install dependencies**

```bash
pip install -r requirements.txt
```

### **3. Required libraries**

Make sure you have the following packages:

```
yfinance
pandas
numpy
scikit-learn
xgboost
```

Install them manually if needed:

```bash
pip install yfinance pandas numpy scikit-learn xgboost
```

---

## **How to Run the Project**

Run the main script:

```bash
python stock_prediction.py
```

The script will:

1. Download 25 years of Asian Paints historical stock data
2. Generate all technical indicators
3. Train Logistic Regression, SVM, and XGBoost models
4. Evaluate each model
5. Predict next-day price movement

---

## **Model Output Example**

```
=========== Logistic Regression ===========
Accuracy: 0.61
Precision: 0.64
Recall: 0.58
F1 Score: 0.60
ROC-AUC: 0.67

Confusion Matrix:
[[145  68]
 [ 91 132]]
```

Similar results are shown for SVM and XGBoost.

---

## **Next-Day Prediction Example**

```
NEXT DAY PREDICTION:
Logistic Regression: UP
SVM: DOWN
XGBoost: UP
```

---

## **Improvement Ideas**

You can further improve model accuracy by:

* Adding more indicators (RSI14, Stochastic, VWAP, OBV)
* Hyperparameter tuning (GridSearchCV or Optuna)
* Ensemble models (VotingClassifier)
* Deep learning (LSTM with technical indicators)
* Using multiple stocks and building a general model


---

## **Author**

Developed by **Praveen**
Feel free to connect and contribute.

---
