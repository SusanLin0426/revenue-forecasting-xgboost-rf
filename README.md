# Revenue Forecasting with XGBoost and Random Forest

This repository contains code and analysis for predicting **monthly revenue levels** of Taiwanese listed firms using machine learning models. The project evaluates the accuracy of **XGBoost** and **Random Forest** across multiple datasets, preprocessing strategies, and industries.

---

## Project Structure
- `Revenue Prediction.ipynb` : Jupyter Notebook with code implementation.
- `Revenue Prediction.pdf` : Full written report with figures, results, and insights.

---

## Research Overview

### Objectives
1. Forecast monthly revenue for **2018–2019** and **2020–2022**.
2. Compare:
   - **XGBoost vs. Random Forest**
   - **Normalized (deflated) vs. raw data**
   - **All industries vs. semiconductor sector**
3. Evaluate models with **RMSE** and **MAE**.
4. Identify **best/worst models** and analyze variable importance.

---

## Methodology
- **Models:** XGBoost, Random Forest  
- **Preprocessing:** 
  - Data cleaning and time-series formatting
  - Standardization (deflation) of revenue series
- **Evaluation Metrics:** RMSE (Root Mean Squared Error), MAE (Mean Absolute Error)

---

## Key Findings
- **XGBoost outperforms Random Forest** across both raw and deflated datasets.
- **Normalization improves accuracy** by reducing noise and outlier effects.
- **Important features:** 
  - Recent months’ lags (t-1, t-2, t-3) capture short-term momentum.
  - Yearly lag (t-12) captures seasonal effects.
- **Best models:** July 2020 (low RMSE/MAE, strong reliance on t-1, t-2).  
- **Worst models:** September 2022 (high RMSE/MAE), partly due to **market shocks** (e.g., semiconductor policy changes, CHIPS Act).  
- **Semiconductor sector analysis:**  
  - Narrowing focus improves accuracy.  
  - Short-term lags (t-1, t-2) are more critical than long seasonal lags.  

---

## Environment
- Python 3.9+
- Jupyter Notebook
- Libraries:
  - `pandas`, `numpy`
  - `scikit-learn`
  - `xgboost`
  - `matplotlib`, `seaborn`
