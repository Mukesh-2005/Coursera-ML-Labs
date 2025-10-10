# 📞 Telecom Customer Classification with K-Nearest Neighbors

This project explores customer segmentation for a telecommunications provider using demographic data. The goal is to predict customer service category based on features such as age, region, marital status, and income using **K-Nearest Neighbors (KNN)** classification.

---
## 🎯 Objective

Predict the service category (`custcat`) for unknown customers based on demographic features. The four service categories are:

1. Basic Service  
2. E-Service  
3. Plus Service  
4. Total Service
---
## 📦 Dataset

- **Source:** [Telecom Dataset](https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-ML0101EN-SkillsNetwork/labs/Module%203/data/teleCust1000t.csv)  
- **Features:** Region, Age, Marital Status, Income, Tenure, etc.  
- **Target:** `custcat` (multi-class label with 4 categories)
---
## 📊 Feature Correlation with Target

| Feature   | Correlation |
|-----------|-------------|
| ed        | 0.1939      |
| tenure    | 0.1667      |
| income    | 0.1345      |
| employ    | 0.1100      |
| marital   | 0.0838      |
| reside    | 0.0820      |
| address   | 0.0679      |
| age       | 0.0569      |
| region    | 0.0238      |
| retire    | 0.0089      |
| gender    | 0.0050      |

Most features show weak correlation with the target, which impacts KNN performance.

---
## 🧪 KNN Classification Results

We experimented with different values of **k** to find the optimal number of neighbors for classification.

| k Value Range     | Best Accuracy | Best k |
|-------------------|---------------|--------|
| 1 to 30           | 0.385         | 30     |
| 1 to 100          | 0.41          | 38     |

- **Test Accuracy (k=4):** 0.32  
- **Test Accuracy (k=6):** 0.31  
- **Best Accuracy (k=30):** 0.385  
- **Best Accuracy (k=38):** 0.41  

These results show that increasing the number of neighbors can improve generalization, with the best performance achieved at **k = 38**.

---
## ⚙️ Model Behavior
### Small k (e.g., k=1)
- Highly sensitive to individual data points  
- Flexible decision boundaries → Overfitting risk  
- High training accuracy, poor generalization

### Large k (e.g., k=38)
- Smoother decision boundaries  
- More generalized predictions  
- Reduced sensitivity to noise  
- Best test accuracy achieved at **k = 38** with **0.41**
---
## ❌ Challenges with KNN

1. **No Feature Learning:** KNN uses raw feature space at inference; cannot optimize or transform features.
2. **Curse of Dimensionality:** Many weakly correlated features dilute distance metrics.
3. **Equal Feature Weighting:** All features contribute equally, even if some are noisy or irrelevant.
---
## 🚀 How to Run

1. Clone the repository  
2. Install dependencies:  
   ```bash
   pip install pandas numpy matplotlib scikit-learn
---

> Built by Mukesh — part of my supervised learning series  
> 📅 Last updated: September 2025
