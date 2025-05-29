# 📈 Natural Gas Forecasting & Credit Risk Modeling

This repository includes a complete set of Python notebooks and scripts designed for:

1. **Forecasting Natural Gas Prices**
2. **Evaluating Storage Contract Value**
3. **Predicting Loan Default Probability**
4. **Optimizing Credit Score Buckets using Dynamic Programming**

---

## 🔍 Project Overview

| Task | Description |
|------|-------------|
| **Task 1** | Time-series forecasting of natural gas prices using linear + seasonal (sine) components |
| **Task 2** | Evaluate contract profitability from injection/withdrawal pricing strategies |
| **Task 3** | Train classification models (Logistic Regression, Decision Tree, Random Forest, XGBoost) for predicting credit default |
| **Task 4** | Use dynamic programming to optimally divide FICO score range into buckets maximizing log-likelihood of default segmentation |

---

## 🧠 Methods Summary

### Task 1: Natural Gas Price Forecasting
- Linear regression over time (days since start)
- Seasonal sinusoidal fitting (1-year period)
- Daily forecast interpolation using `interpolate()`
- Visualization of smoothed estimate and fit curve

### Task 2: Gas Contract Pricing Model
- Given injection/withdrawal dates, rates, and costs:
  - Simulate storage volume dynamics
  - Accumulate costs (purchase, injection, storage)
  - Return total contract profit or loss

### Task 3: Loan Default Classifiers
- Uses `Task34_Loan_Data.csv`
- Models trained:  
  - Logistic Regression  
  - Decision Tree  
  - Random Forest  
  - XGBoost
- Evaluation metrics:
  - Accuracy
  - AUC (Area Under ROC Curve)

### Task 4: FICO Score Bucketing
- Calculate cumulative default counts for each score
- Apply dynamic programming to split the score into `r = 10` buckets
- Maximize log-likelihood assuming binomial model of default
- Output: best cut-off points between score intervals
