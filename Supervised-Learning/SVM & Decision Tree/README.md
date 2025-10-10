# 🛡️ Credit Card Fraud Detection

This project focuses on building machine learning models to detect fraudulent credit card transactions using the [Credit Card Fraud Detection dataset](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud) from Kaggle. The dataset is highly imbalanced, with only **0.172%** of transactions labeled as fraud.

## 📦 Dataset Overview

- **Total transactions:** 284,807  
- **Fraudulent transactions:** 492  
- **Legitimate transactions:** 284,315  
- **Features:** 30 anonymized variables including `V1` to `V28`, `Amount`, and `Time`  
- **Target variable:** `Class` (0 = legitimate, 1 = fraud)
  
![plot](https://github.com/Mukesh-2005/Coursera-ML-Labs/blob/main/Supervised-Learning/SVM%20&%20Decision%20Tree/graphs/fraud%20Detection.png?raw=true)

## ⚠️ Class Imbalance

Due to the extreme imbalance in the target variable, special care is taken during model training:

- **Class weights** are used to penalize misclassification of the minority class  
- **ROC-AUC** is used as the primary evaluation metric to assess model performance beyond simple accuracy

## 🌳 Decision Tree Classifier

- Configured with `max_depth=4`  
- Trained using **balanced sample weights**  
- Shallow depth prevents overfitting and improves interpretability  
- **ROC-AUC Score:** 0.939

## 💡 Support Vector Machine (Linear SVC)

- Uses a **linear kernel** with hinge loss  
- Trained with **balanced class weights**  
- Intercept term disabled for simplicity  
- Performs well in high-dimensional spaces  
- **ROC-AUC Score:** 0.986

## 🧪 Evaluation Strategy

- **Stratified sampling** used to preserve class distribution  
- **ROC-AUC** chosen for robustness in imbalanced classification  
- Features are **standardized** and optionally **normalized** for consistent scaling

## 🔍 Feature Selection Experiment

Top 6 most correlated features with fraud label:  
`V17`, `V14`, `V12`, `V10`, `V16`, `V3`

### Retrained Models:

- **Decision Tree:** ROC-AUC remained at 0.939 — benefits from focused, high-signal features  
- **SVM:** ROC-AUC dropped to 0.937 — suggests SVMs thrive in higher-dimensional spaces

## 💡 Key Insights

- SVM outperforms Decision Trees with full feature set  
- Decision Trees maintain strong performance with selected features  
- SVMs may require more features to construct effective decision boundaries

## 🚀 How to Run

1. Clone the repository  
2. Install required libraries:  
   ```bash
   pip install -r requirements.txt


> Built by Mukesh — part of my supervised learning series  
> 📅 Last updated: September 2025
