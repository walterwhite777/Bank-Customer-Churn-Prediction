# 🏦 Bank Customer Churn Prediction  

## 📌 Overview  
This project predicts **customer churn** (whether a bank customer will leave) using machine learning.  
We implemented and compared Logistic Regression, Random Forest, and XGBoost, and enhanced the pipeline with advanced evaluation metrics, class imbalance handling, and model interpretability (SHAP).  

---

## 📊 Dataset  
- **Source:** [Kaggle – Bank Customer Churn Dataset](https://www.kaggle.com/datasets/radheshyamkollipara/bank-customer-churn)  
- **Size:** 10,000 customers  
- **Target Variable:** `Exited` (1 = churned, 0 = stayed)  

---

## 🚀 Work Done  
- **Data Preprocessing**
  - Dropped irrelevant columns (`CustomerId`, `Surname`, `RowNumber`).  
  - One-hot encoding for categorical features (`Gender`, `Geography`, `Card Type`).  
  - Applied **SMOTE** to handle class imbalance.  

- **Modeling**
  - Implemented **Logistic Regression, Random Forest, XGBoost**.  
  - Compared models on Accuracy, Precision, Recall, and F1-score.  
  - **Logistic Regression** emerged as the best model.  

- **Advanced Evaluation**
  - ROC-AUC, Precision-Recall AUC, Balanced Accuracy.  
  - Plots: ROC Curve, Precision-Recall Curve, Confusion Matrix.  

- **Interpretability**
  - SHAP (SHapley Additive Explanations) for feature importance.  
  - Identified **top drivers of churn** (e.g., complaints, inactivity, products held).  

- **Model Persistence**
  - Saved trained model (`model.pkl`) and scaler (`scaler.pkl`) with `joblib`.  

---

## 📈 Results (Best Model: Logistic Regression)  
| Metric              | Score   |
|----------------------|---------|
| Accuracy             | **0.991** |
| Precision (Class 1)  | **0.995** |
| Recall (Class 1)     | **0.958** |
| F1-Score (Class 1)   | **0.976** |
| ROC-AUC              | **0.998** |
| PR-AUC               | **0.995** |
| Balanced Accuracy    | **0.979** |

---
