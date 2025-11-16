# 📊 Regularization in Linear Regression – Evaluation Metrics Lab

This lab investigates how regularization techniques—**Ridge (L2)** and **Lasso (L1)**—affect linear regression performance under two conditions:
1. A simple 1-D dataset with and without outliers
2. A synthetic high-dimensional dataset with known informative features

The core focus is on **evaluation metrics**—how different models perform and generalize based on quantitative indicators like R², MAE, MSE, and RMSE.

---

## 🎯 Goal

To understand and compare model robustness, generalization, and feature selection capabilities using **evaluation metrics** as the primary lens.

---

## 📁 Lab Structure

### 1️⃣ Simple Regression with Outliers

- Generated synthetic data: \( y = 4 + 3X + \text{noise} \)
- Injected outliers at high \( X \) values
- Trained:
  - `LinearRegression`
  - `Ridge(alpha=1)`
  - `Lasso(alpha=0.2)`
- Compared fitted lines on clean vs. noisy data

### 2️⃣ High-Dimensional Regression (100 Features)

- Used `make_regression(n_samples=100, n_features=100, n_informative=10, noise=10, coef=True)`
- Trained:
  - `LinearRegression`
  - `Ridge(alpha=1)`
  - `Lasso(alpha=0.1)`
- Compared predictions, coefficients, and residuals
- Used Lasso for feature selection and retrained models on reduced feature set

---

## 📊 Evaluation Metrics Used

| Metric | Description |
|--------|-------------|
| **R² Score** | Measures proportion of variance explained |
| **Explained Variance** | Similar to R², but less sensitive to bias |
| **Mean Absolute Error (MAE)** | Average absolute difference between predictions and actual values |
| **Mean Squared Error (MSE)** | Penalizes larger errors more heavily |
| **Root Mean Squared Error (RMSE)** | Square root of MSE for interpretability |

### 🔍 Metric Comparison (Before Feature Selection)

| Model         | R²     | MAE     | MSE     | RMSE    |
|---------------|--------|---------|---------|---------|
| Linear        | ≈ 0.401 | ≈ 77.75 | ≈ 9855  | ≈ 99.27 |
| Ridge         | ≈ 0.408 | ≈ 76.96 | ≈ 9744  | ≈ 98.71 |
| Lasso         | ≈ 0.982 | ≈ 13.89 | ≈ 304.6 | ≈ 17.45 |

### ✅ After Feature Selection (Lasso-selected features)

- All models achieved R² ≈ 0.98
- MAE and RMSE dropped significantly for Linear and Ridge
- Performance matched Lasso with fewer features

---

## 📈 Visual Diagnostics

- **Regression line plots** (with and without outliers)
- **Coefficient comparison**: True vs. predicted
- **Residual plots**: Ideal − predicted
- **Feature selection thresholding** using Lasso coefficients

---

## 🧠 Key Takeaways

### 🔹 Outlier Sensitivity
- LinearRegression is highly sensitive to extreme values.
- Lasso showed better robustness due to L1 penalty.

### 🔹 Feature Selection
- Lasso effectively identified ~9 of 10 informative features.
- Retraining Linear/Ridge on selected features improved performance dramatically.

### 🔹 Metric-Driven Insights
- Evaluation metrics revealed model weaknesses and strengths more clearly than visual inspection alone.
- RMSE and MAE were especially useful for quantifying prediction error.

---
>Built by Mukesh — part of My Evaluation Metrics series.
📅 Last updated: November 2025

