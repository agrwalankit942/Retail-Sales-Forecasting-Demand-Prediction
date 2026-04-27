<img width="840" height="840" alt="image" src="https://github.com/user-attachments/assets/bb9b2e45-819a-493a-b00e-56e4106feda4" />
<img width="840" height="840" alt="image" src="https://github.com/user-attachments/assets/179d64b6-ebeb-4353-bc33-1cbee1860bae" />

<img width="840" height="840" alt="image" src="https://github.com/user-attachments/assets/9858d976-920f-4410-a2d4-e2f95791cfc6" />


# 📊 Retail Demand Forecasting using Time Series Models

## 📌 Project Overview

This project focuses on forecasting product demand using time series analysis on a retail dataset. The goal is to build accurate predictive models to support better inventory management and business decision-making.

---

## 📂 Dataset Description

The dataset contains historical product demand along with additional influencing factors:

* `Product_id`
* `Product_Code`
* `Warehouse`
* `Product_Category`
* `Date`
* `Order_Demand` *(Target Variable)*
* `Open`
* `Promo`
* `StateHoliday`
* `SchoolHoliday`
* `Petrol_price`

---

## 🧹 Data Preprocessing

The following preprocessing steps were performed:

* Converted `Order_Demand` from string to numeric
* Converted `Date` to proper date format
* Removed missing values
* Sorted data chronologically
* Handled outliers using IQR-based capping
* Applied **log transformation** to reduce skewness

---

## 🔧 Feature Engineering

* Extracted time-based features (Year, Month, etc.)
* Created lag variables and rolling statistics
* Added trend component
* Considered external factors:

  * Promotions (`Promo`)
  * Holidays (`StateHoliday`, `SchoolHoliday`)
  * Petrol price (`Petrol_price`)

---

## 📈 Exploratory Data Analysis (EDA)

* Visualized demand trends over time
* Identified seasonality patterns
* Detected skewness in raw data
* Improved distribution using log transformation

---

## 🤖 Models Used

### 1️⃣ ARIMA (AutoRegressive Integrated Moving Average)

* Captures temporal dependencies and autocorrelation
* Final model: **ARIMA(2,0,3)**

### 2️⃣ ETS (Exponential Smoothing)

* Captures level and trend
* Model used: **ETS(M,N,N)**

---

## 📊 Evaluation Metrics

Models were evaluated using:

* RMSE (Root Mean Square Error)
* MAE (Mean Absolute Error)
* sMAPE (Symmetric Mean Absolute Percentage Error)
* MASE (Mean Absolute Scaled Error)

---

## 🔍 Residual Diagnostics

* **ARIMA Model**

  * Ljung-Box p-value: 0.352 ✅
  * Residuals behave like white noise

* **ETS Model**

  * Ljung-Box p-value: 0.021 ❌
  * Residuals show autocorrelation

---

## 🏆 Results

* ARIMA outperformed ETS across evaluation metrics
* ARIMA satisfied statistical assumptions
* ETS failed to capture all underlying patterns

---

## ✅ Conclusion

The **ARIMA model** is selected as the best-performing model for forecasting product demand due to its superior accuracy and statistically valid residual behavior.

---

## 🚀 Future Scope

* Use ARIMAX with external variables
* Apply machine learning models (Random Forest, XGBoost)
* Perform time-series cross-validation
* Deploy model for real-time forecasting

---

## 🛠️ Technologies Used

* R Programming
* Libraries:

  * `forecast`
  * `ggplot2`
  * `tidyverse`
  * `Metrics`
  * `lubridate`

---

## 📌 How to Run

1. Load dataset in R
2. Run preprocessing script
3. Apply feature engineering
4. Train ARIMA and ETS models
5. Evaluate using metrics
6. Visualize results

---

## 👤 Author

**Ankit Agrawal**

---

