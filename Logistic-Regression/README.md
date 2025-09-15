# 📊 Logistic Regression Churn Prediction Lab

This repository contains a guided lab session focused on predicting customer churn using logistic regression. The scenario simulates a telecommunications company aiming to identify customers likely to leave their land-line service for cable competitors.

---
## 🧠 Objective

To build a classification model that predicts customer churn based on demographic and service usage features, and to evaluate its performance using probabilistic metrics like `log_loss`.

---
## 📁 Dataset

The dataset used is a hypothetical customer churn dataset provided via IBM Skills Network. Each row represents a customer and includes:
- Demographic details (age, education, address)
- Service usage (tenure, callcard, equip)
- Churn label (0 = stay, 1 = leave)

Data is loaded directly from:
"https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-ML0101EN-SkillsNetwork/labs/Module%203/data/ChurnData.csv"

---
## ⚙️ Model

A logistic regression classifier is trained to:
- Interpret feature coefficients
- Predict churn probabilities
- Classify customers based on a threshold (default: 0.5)

---
## 📈 Evaluation

Model performance is assessed using:
- **Log Loss**: Measures confidence and calibration of predictions  
  → Current result: `log_loss = 0.78` (indicates room for improvement)
- **Predicted Probabilities**: Used to understand model certainty
- **Feature Coefficients**: Visualized to interpret feature impact

---
## 🧪 Key Learnings

- Positive coefficients increase likelihood of churn
- Negative coefficients decrease it
- Log loss penalizes confident wrong predictions more than uncertain ones
- Adding features can improve or worsen calibration

---
## 🚀 Next Steps

This lab serves as a foundation for future personal projects. Upcoming work will include:
- Feature engineering and selection
- Threshold tuning and calibration
- Model comparison and interpretability

Stay tuned for original machine learning projects built from scratch!
