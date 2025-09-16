
# 📈 Multiple Linear Regression – Fuel Consumption & CO₂ Emissions

This lab extends the previous Simple Linear Regression model by incorporating multiple features to predict CO₂ emissions more accurately. The goal is to demonstrate how using more than one predictor can improve model performance.

---

## 🔍 Feature Selection

Unlike the simple model which used only `FUELCONSUMPTION_COMB`, this version uses two features:

- `ENGINESIZE`
- `CYLINDERS`

These were selected based on their strong positive correlation with `CO2EMISSIONS`, confirmed through visualizations and correlation analysis.

---
## 📸 Visualizations

### Fuel Consumption vs CO₂ Emissions
![Fuel vs Emission](https://github.com/Mukesh-2005/Coursera-ML-Labs/blob/main/Multi-Linear-Regression/charts/Fuelconsumption_comp_mpg.png)
*Higher MPG → Lower emissions. A clear negative correlation.*

### Engine Size vs CO₂ Emissions
![Engine vs Emission](https://github.com/Mukesh-2005/Coursera-ML-Labs/blob/main/Multi-Linear-Regression/charts/Engine%20Size.png)  
*Larger engines tend to emit more CO₂. Strong positive correlation.*

###💡 Bonus Tip
Note: A 3D plot was also attempted to visualize the combined effect of both features, but due to complexity and limited interpretability, 2D plots were preferred for clarity

---
## 📊 Model Performance Comparison

| Model Type              | MSE       | R² Score |
|-------------------------|-----------|----------|
| Simple Linear Regression | 797.43    | 0.81     |
| Multiple Linear Regression | 466.11    | 0.89     |

The multiple linear regression model significantly outperforms the simple model, reducing error and improving predictive accuracy.

---

## 🛠️ Technologies Used

- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- scikit-learn
---

## 🚀 How to Run

1. Clone the repository  
2. Navigate to the `Multiple-Linear-Regression` folder  
3. Install dependencies:  
---

## 📌 Next Steps

- Add more features like `FUELCONSUMPTION_CITY` or `FUELCONSUMPTION_HWY`
- Try polynomial regression or regularization techniques
