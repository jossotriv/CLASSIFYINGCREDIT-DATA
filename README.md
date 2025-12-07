# Credit Score Classification — CSCA 5622 Supervised Learning Project

This repository contains a supervised machine learning project completed for **CSCA 5622 — Machine Learning** at the University of Colorado Boulder. The goal of this project is to build a predictive model capable of classifying an individual's **credit score category** based on mixed financial, behavioral, and demographic attributes.

** Important note is that the Training and Test Data Set are too large to upload to GitHub, please use the link: https://www.kaggle.com/datasets/parisrohan/credit-score-classification/data to access the data if you'd like to replicate the project. **

---

## 📌 Project Overview

This project explores multiple supervised learning classification algorithms and feature-engineering strategies to determine the most accurate and robust model for credit score prediction. We compare:

- Logistic Regression  
- Gradient Boosting  
- LightGBM  
- Random Forest  ← **Top Performer** 🎯

All models were evaluated using:
- **F1 Score** (primary metric due to class imbalance)
- **Accuracy**
- Confusion matrices
- ROC & AUC analysis

Random Forest consistently achieved the **highest F1 Scores and strongest ROC performance** across all feature sets.

---

## 🧠 Machine Learning Task

- **Type:** Supervised Learning  
- **Category:** Multi-class Classification  
- **Target Variable:** `Credit_Score` (Good, Standard, Poor)  
- **Features:** 35+ engineered numeric & categorical attributes  

---

## 📊 Dataset Information

- **Source:** Kaggle — “Credit Score Classification” by Rohan Paris  
- **Training Samples:** ~75,000 customers  
- **Test Samples:** ~28,000 customers  
- **Feature Types:**  
  - 18+ numeric features  
  - 12+ categorical features  
  - Multiple engineered features such as loan flags and credit history months  
- **Note:** Test dataset includes **10 distinct months**, while training has **8**, requiring careful handling of unseen categories.

📌 Full APA Citation:
> Paris, R. (2020). *Credit Score Classification dataset* [Data set]. Kaggle. https://www.kaggle.com/datasets/parisrohan/credit-score-classification/data

---

## 🧼 Data Cleaning

The dataset contained:
- Header duplication rows
- Corrupted strings (e.g., `"__"` and `"!@#$%"`)
- Unrealistic values (e.g., age > 100, 1000+ credit cards)
- Salary mismatches between monthly vs annual income

Cleaning actions:
- Value clipping, imputation, type fixes
- Loan feature engineering
- Removal of high-noise identifiers

---

## 🔍 EDA Highlights

- Credit score classes are moderately imbalanced  
- Higher income, lower debt, and responsible payment behavior correlate strongly with good scores  
- Strong nonlinear patterns exist → tree models outperform linear models  

---

## 🚀 Results Summary

| Feature Set | Best Model | Accuracy | F1 Score |
|------------|------------|----------|---------|
| Total Features | Random Forest | **0.7759** | **0.7603** |
| Top Features Simple | Random Forest | **0.7729** | **0.7579** |
| Selected Features Mixed | Random Forest | **0.7736** | **0.7580** |
| Top 20 Features Mixed | Random Forest | **0.7536** | **0.7339** |

📌 Random Forest is the **recommended model for deployment**.

---

## 🔮 Future Improvements

- Hyperparameter tuning (Bayesian Optimization)
- Ensemble stacking of top models
- SHAP-based fairness and interpretability
- Monitoring for temporal drift (seasonality)

---

## 📁 Repository Structure
