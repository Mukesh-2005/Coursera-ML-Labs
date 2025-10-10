# 🚗 Simple Linear Regression – Fuel Consumption & CO₂ Emissions

This project is a personalized implementation of the **Simple Linear Regression** lab from the Coursera Machine Learning course. The goal is to predict **CO₂ emissions** of vehicles based on selected features using scikit-learn's linear regression model.

---


## 📊 Dataset overview

**FuelConsumptionCo2.csv**  
This dataset contains fuel consumption ratings and estimated CO₂ emissions for light-duty vehicles sold in Canada.

- Source: [IBM Skills Network Lab Dataset](https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-ML0101EN-SkillsNetwork/labs/Module%202/data/FuelConsumptionCo2.csv)
- Loaded directly via `pandas.read_csv()` from the URL


The dataset includes specifications and fuel consumption ratings for light-duty vehicles sold in Canada. Key features include:

- `ENGINE SIZE`
- `CYLINDERS`
- `FUEL CONSUMPTION COMBINED (L/100 km)`
- `CO2 EMISSIONS (g/km)` ← Target variable

---

## 🔍 Feature Selection

To identify the most predictive features for CO₂ emissions, I computed the correlation matrix and visualized key variables:

- `FUELCONSUMPTION_COMB` showed the strongest positive correlation with CO₂ emissions  
- `ENGINESIZE` and `CYLINDERS` also had strong linear relationships  
- Visualizations (histograms and scatter plots) helped confirm the suitability of these features for regression

This guided my decision to use `FUELCONSUMPTION_COMB` as the primary input for the simple linear regression model.

![Best Features](https://raw.githubusercontent.com/Mukesh-2005/Coursera-ML-Labs/main/Linear-Regression/images/Best%20features.png)

---

## 🧠 What I Did

- Explored and cleaned the dataset using **Pandas**
- Selected relevant features for prediction
- Built a **Simple Linear Regression** model using **scikit-learn**
- Trained and tested the model with different train-test splits
- Evaluated performance using:
  - Mean Squared Error (MSE)
  - Root Mean Squared Error (RMSE)
- Visualized predictions and residuals using **Matplotlib**

---

## 🔍 Key Learnings

- How to implement and interpret simple linear regression
- The impact of feature selection on model accuracy
- How train-test split ratios affect performance
- How to evaluate regression models using standard metrics

---

## 📁 Files Included

- `notebook.ipynb`: Full implementation with code, comments, and visualizations
- `requirements.txt`: Python packages used
- `FuelConsumption.csv`: Dataset used (or link to source)

---

## 📌 Next Steps

- Try multiple linear regression with more features
- Explore polynomial regression for non-linear relationships
- Compare performance with other regression models (e.g., Ridge, Lasso)

---

> Built by Mukesh — part of my supervised learning series  
> 📅 Last updated: September to October 2025
