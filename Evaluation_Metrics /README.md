# 🧪 Breast Cancer Classification – Evaluation Metrics Lab

This lab explores the robustness of classification models under noisy conditions using the Breast Cancer Wisconsin dataset. The focus is on **evaluation metrics**—accuracy, precision, recall, F1-score, and confusion matrices—to assess model performance and generalization.

---

## 📊 Objective

To compare how **K-Nearest Neighbors (KNN)** and **Linear Support Vector Machine (SVM)** classifiers perform on clean vs noisy data, and to interpret their behavior using detailed evaluation metrics.

---

## 🧬 Dataset

- **Source**: `sklearn.datasets.load_breast_cancer`
- **Features**: 30 numeric measurements of cell nuclei
- **Target**: Binary classification – `malignant` (0) vs `benign` (1)

---

## 🧼 Preprocessing

- **Standardization**: Applied `StandardScaler` to normalize features.
- **Noise Injection**: Added Gaussian noise (`noise_factor = 0.5`, `seed = 42`) to simulate real-world data corruption.

---

## 📈 Visualization

- Compared original vs noisy feature distributions using:
  - Histograms
  - Line plots
  - Scatterplots

**Observation**: Noise made skewed features more symmetric, resembling Gaussian distributions.

---

## 🧠 Modeling

Two classifiers were trained and evaluated:

| Model | Parameters |
|-------|------------|
| KNN   | `n_neighbors=5` |
| SVM   | `kernel='linear'`, `C=1` |

Each model was trained on:
- **Clean data** (`X_scaled`)
- **Noisy data** (`X_noisy`)

---

## 🧪 Evaluation Metrics

### ✅ Accuracy

| Model | Dataset | Train Accuracy | Test Accuracy |
|-------|---------|----------------|---------------|
| KNN   | Clean   | ≈ 0.922        | ≈ 0.959       |
| SVM   | Clean   | ≈ 0.965        | ≈ 0.965       |
| KNN   | Noisy   | ≈ 0.626        | ≈ 0.632       |
| SVM   | Noisy   | ≈ 0.628        | ≈ 0.637       |

### 📊 Confusion Matrices

Plotted as heatmaps for each model and dataset split. Revealed class-wise prediction strengths and weaknesses.

### 📋 Classification Reports

Included:
- **Precision**
- **Recall**
- **F1-score**
- **Support**

**Key Insight**:  
On noisy data, both models collapsed to predicting the majority class (`benign`). Recall for `malignant` dropped to ≈ 0.00, which is critical in medical diagnosis.

---

## 🧠 Analysis & Takeaways

- **SVM outperformed KNN** on clean data across all metrics.
- **False negatives** (missed malignant cases) are the most dangerous error.
- **Noise sensitivity**: Both models failed to generalize under noise, highlighting the importance of robust preprocessing.
- **Evaluation metrics** provided deeper insights than accuracy alone—especially in imbalanced or noisy scenarios.

---

## 📌 Conclusion

This lab emphasizes the **importance of evaluation metrics** in model assessment. Accuracy alone can be misleading—confusion matrices and class-wise metrics are essential for understanding real-world impact, especially in sensitive domains like healthcare.

---

