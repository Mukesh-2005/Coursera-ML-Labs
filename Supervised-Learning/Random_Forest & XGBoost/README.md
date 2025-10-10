# 🏠 California Housing Price Prediction

This project compares two regression models — **Random Forest** and **XGBoost** — on the California Housing dataset. The goal is to predict median house values based on various features such as income, location, and population density.

---

## 📦 Dataset

- **Source**: `sklearn.datasets.fetch_california_housing()`
- **Target Variable**: Median house value (`y`)
- **Feature Matrix**: 8 numerical features (`X`)

---

## 🧠 Models Used

- `RandomForestRegressor` (n_estimators = 100)
- `XGBRegressor` (n_estimators = 100)

Both models were trained and evaluated on the same train-test split for fair comparison.

---

## ⚙️ Training & Evaluation Metrics

| Model           | MSE     | RMSE    | R² Score | Train Time | Test Time |
|----------------|---------|---------|----------|------------|-----------|
| Random Forest  | 0.2556  | 0.5055  | 0.8050   | 13.111 s   | 0.187 s   |
| XGBoost        | 0.2226  | 0.4717  | 0.8301   | 0.210 s    | 0.006 s   |

- **RMSE** is interpreted as the average prediction error in the same units as the target.
- **R² Score** indicates how well the model explains the variance in the data.
- **Training Time** and **Testing Time** highlight computational efficiency.

---

## 📊 Residual Analysis

- **XGBoost Residual Std Dev**: `0.4717`
- Most predictions from both models fall within ±1 standard deviation of the actual values.
- **Random Forest** respects the upper bound of the target values, while **XGBoost** occasionally overshoots — a sign of its aggressive boosting behavior.
![Random Forest & XGBoost](https://github.com/Mukesh-2005/Coursera-ML-Labs/blob/main/Random_Forest%20%26%20XGBoost/visuals/Random%20vs%20XGBoost.png)
---

## 🧠 Key Learnings

- **XGBoost** achieved slightly better accuracy and significantly faster training/testing times.
- **Random Forest** provided stable predictions and stayed within the target range.
- RMSE of ~0.50 indicates moderate predictive accuracy, with average errors around 10% of the target range.
- Visual residual plots helped diagnose model behavior near the extremes.

---

## 📁 Future Work

- Explore feature engineering to improve model performance.
- Apply cross-validation for more robust evaluation.
- Tune hyperparameters (e.g., `max_depth`, `learning_rate`, `subsample`) for XGBoost.
- Investigate ensemble stacking or blending strategies.

---

## 🧪 Requirements

```bash
pip install -r requirements.txt
```
> Built by Mukesh — part of my supervised learning series  
> 📅 Last updated: September to October 2025
