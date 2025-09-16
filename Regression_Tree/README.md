# 🚕 Regression Tree Analysis — NYC Taxi Trip Data

This notebook explores regression tree models applied to the `yellow-tripdata.csv` dataset, aiming to predict a continuous target variable based on trip-related features. The analysis includes model training, evaluation, and visual diagnostics across different tree depths.

---

## 📌 Objectives

- Train regression trees with varying depths (`max_depth=4` and `max_depth=8`)
- Evaluate model performance using MSE and R² Score
- Visualize residual patterns and tree structure
- Analyze feature relevance using correlation

---

## 📊 Model Performance Summary

| Depth | MSE     | R² Score |
|-------|---------|----------|
| 4     | 25.337  | 0.024    |
| 8     | 25.587  | 0.015    |

> Both models show poor predictive performance, with R² values below 0.03 — indicating minimal variance explained by the features.

---

## 📉 Residuals vs. Predicted Values

- Residuals are widely scattered, especially for predicted values between 10–20
- No clear improvement with increased depth
- Suggests potential heteroscedasticity and model inadequacy
- Red dashed line at zero helps visualize bias and error spread

![Residuals vs. Predicted Values](https://github.com/Mukesh-2005/Coursera-ML-Labs/blob/main/Regression_Tree/Visuals/Residuals.png)
---

## 🌲 Tree Structure Visualization

- Trees split on features like `X[7]`, `X[12]`, `X[0]`, `X[5]`, etc.
- Leaf nodes show predicted values and sample counts
- Squared error values indicate local fit quality
- Deeper trees capture more splits but do not improve generalization

![Regression Tree Structure](https://github.com/Mukesh-2005/Coursera-ML-Labs/blob/main/Regression_Tree/Visuals/Regresion_tree.png)
---

## 📊 Feature Correlation Analysis

- Highest correlation with target: ~0.20
- Most features show weak linear relationships
- Top correlated features: `fare_amount`, `trip_distance`, `tolls_amount`
- Features like `VendorID`, `store_and_fwd_flag`, and `RatecodeID` show negligible influence

> Correlation-based feature selection reveals limited signal strength in the dataset, which likely contributes to poor model performance.

---

## 🧠 Interpretation

- Regression trees struggled to extract meaningful patterns from the data
- Weak feature-target relationships and noisy inputs limit model effectiveness
- Increasing depth led to overfitting without performance gains
- Visual diagnostics confirm lack of structure and high residual variance

---

## 🚀 Next Steps

- Engineer new features (e.g. trip duration, time of day, pickup/dropoff zones)
- Try ensemble methods like Random Forest or Gradient Boosting
- Explore regularization and feature transformations
- Investigate target variable quality and distribution

---

## 📁 Dataset

- Source: [yellow-tripdata.csv](https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/pu9kbeSaAtRZ7RxdJKX9_A/yellow-tripdata.csv)
- Format: CSV
- Features: Trip metadata, fare details, location IDs, and payment info

---

> Built by Mukesh — part of my supervised learning series  
> 📅 Last updated: September 2025
