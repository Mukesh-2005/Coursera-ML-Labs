# 🧠 Multi-Class Logistic Regression: Obesity Risk Prediction

This repository contains a machine learning notebook that explores three strategies for multi-class classification using logistic regression. The task is to predict obesity risk levels based on lifestyle and health-related features.

## 📊 Objective

To compare the performance of:
- **One-vs-All (OvA)** strategy
- **One-vs-One (OvO)** strategy
- **Multinomial (Softmax)** logistic regression

...on a real-world-style dataset for predicting obesity levels.

## 📁 Dataset

The dataset is sourced from [IBM Skills Network](https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/GkDzb7bWrtvGXdPOfk6CIg/Obesity-level-prediction-dataset.csv) and includes:
- Demographics: Age, Gender, Height, Weight
- Lifestyle habits: Physical activity, eating frequency, transportation mode
- Target variable: `NObeyesdad` (7 obesity risk categories)

## ⚙️ Preprocessing

- **Standardization** of continuous features
- **One-hot encoding** of categorical variables
- **Label encoding** of target variable
- Train-test split with stratification

## 🧪 Models & Evaluation

### 1️⃣ One-vs-All (OvA)
- Trains one binary classifier per class
- Accuracy: **76.12%**
- Log Loss: **0.7876**

### 2️⃣ One-vs-One (OvO)
- Trains binary classifiers for every pair of classes
- Accuracy: **92.2%**
- `predict_proba` not supported → log loss not computed

### 3️⃣ Multinomial (Softmax)
- Native multi-class logistic regression using softmax
- Accuracy: **87.94%**
- Log Loss: **0.427**

## 📈 Insights

- OvO achieved the highest accuracy but lacks probability calibration
- Multinomial gave the best log loss, indicating well-calibrated predictions
- OvA is simpler but struggled with class imbalance

## 🚀 Technologies Used

- Python 3.10
- pandas, numpy, matplotlib, seaborn
- scikit-learn (LogisticRegression, OneVsOneClassifier, metrics)

## 🛠️ Setup

Install dependencies with:

```bash
pip install -r requirements.txt
