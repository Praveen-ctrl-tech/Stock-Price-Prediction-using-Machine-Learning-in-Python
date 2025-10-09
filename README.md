# 📈🤖 Stock Price Prediction using Machine Learning in Python

This project predicts whether buying a particular stock (Tesla in this case) will be **profitable or not** using **Machine Learning** and **Python**.  
It utilizes historical stock data (2010–2020) and focuses on generating **buy/sell signals** through data analysis, feature engineering, and model training.

---

## 🔍 Project Overview

The primary goals of this project are to:

- Analyze and visualize historical stock data  
- Engineer new predictive financial features  
- Build machine learning models to predict next-day price movements  
- Compare model performance and interpret the results

---

## 📁 Dataset

The dataset used contains **Tesla stock prices** from **January 2010 to December 2020**.  
It includes the following columns:

| Column | Description |
|---------|-------------|
| `Date` | Date of record |
| `Open` | Opening price of the stock |
| `High` | Highest price of the day |
| `Low` | Lowest price of the day |
| `Close` | Closing price of the day |
| `Adj Close` | Adjusted closing price |
| `Volume` | Number of shares traded |

💡 **Note:**  
- Stock markets are closed on weekends and holidays, so some dates are missing.  
- The `Adj Close` column was found to duplicate `Close`, and was dropped during preprocessing.

---

## 🛠️ Technologies Used

| Library | Purpose |
|----------|----------|
| `Python` | Programming language |
| `pandas`, `numpy` | Data handling and numerical computation |
| `matplotlib`, `seaborn` | Data visualization and trend analysis |
| `scikit-learn` | Machine learning models and preprocessing |
| `xgboost` | Advanced boosting algorithm for high-performance prediction |

---

## 🔄 Workflow

### 🧹 **1. Data Preprocessing**
- Load and inspect Tesla stock data  
- Handle redundant and missing columns  
- Extract date-based features (`day`, `month`, `year`)  
- Add a **quarter-end flag** (`is_quarter_end`)  
- Create derived features:
  - `open-close` → Difference between opening and closing prices  
  - `low-high` → Daily price volatility  
  - `target` → 1 if next day’s closing price is higher, else 0

### 📊 **2. Exploratory Data Analysis (EDA)**
- Visualize closing price trends over time  
- Plot yearly average price changes  
- Study price behavior at quarter ends  
- Identify outliers using boxplots  
- Visualize correlations using heatmaps

### ⚙️ **3. Feature Engineering**
- Select relevant input features:
  - `open-close`, `low-high`, `is_quarter_end`  
- Normalize the data using **StandardScaler**
- Split into training (90%) and validation (10%) sets

### 🤖 **4. Model Building**
Trained the following machine learning models:

| Model | Description |
|--------|--------------|
| `Logistic Regression` | Baseline classification model |
| `Support Vector Machine (SVC)` | Polynomial kernel-based classifier |
| `XGBoost Classifier` | Boosting algorithm for higher accuracy |

### 🧾 **5. Evaluation**
- Evaluated models using **ROC-AUC Score**
- Plotted **Confusion Matrix** for validation results
- Compared model performance

---

## 📈 Results

| Model | Training AUC | Validation AUC |
|--------|---------------|----------------|
| Logistic Regression | ~0.52 | ~0.54 |
| SVC (Polynomial) | ~0.47 | ~0.45 |
| XGBoost | ~0.96 | ~0.57 |

🧠 **Insights:**
- XGBoost performs best but tends to **overfit**.  
- Logistic Regression generalizes better despite lower accuracy.  
- The model accuracy (~57%) is only slightly above random guessing, showing the complexity of stock prediction.

---

## 📊 Visualizations

- **Tesla Stock Price Trend (2010–2020)**  
- **Distribution and Box Plots** for OHLC and Volume  
- **Yearly Average Bar Charts**  
- **Quarter-End Performance Comparison**  
- **Correlation Heatmap**  
- **Confusion Matrix for Model Evaluation**

---

## ⚙️ Installation

```bash
# Clone the repository
git clone https://github.com/your-username/Stock-Price-Prediction-using-Machine-Learning.git

# Navigate to the project directory
cd Stock-Price-Prediction-using-Machine-Learning

# Install required libraries
pip install -r requirements.txt
