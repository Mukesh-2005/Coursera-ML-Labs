# 🌐 Principal Component Analysis (PCA) — Visual & Intuitive Exploration

This repository demonstrates PCA through two hands-on parts:  
- **Part I**: Geometric intuition using synthetic 2D data  
- **Part II**: Dimensionality reduction and visualization using the Iris dataset  
Bonus: 3D PCA visualization with synthetic 4D data using Matplotlib and Plotly.

---

## 📁 Structure

- `pca_2d_synthetic.ipynb` — PCA on linearly correlated 2D data
- `pca_iris_dim_reduction.ipynb` — PCA on Iris dataset with explained variance
- `pca_3d_visualization.ipynb` — PCA on synthetic 4D data with 3D plots

---

## 🧪 Part I — PCA on Synthetic 2D Data

**Goal:** Understand PCA geometrically by projecting data onto principal axes.

### 🔧 Steps:
- Generated 200 samples from a bivariate normal distribution  
- Visualized raw data using scatter plot  
- Applied PCA with `n_components=2`  
- Manually projected data onto PC1 and PC2  
- Plotted projections to show principal directions

### 📌 Insight:
- PC1 captures the direction of maximum variance  
- PC2 is orthogonal and captures residual variance

---

## 🌸 Part II — PCA on Iris Dataset

**Goal:** Apply PCA for dimensionality reduction and visualize class separation.

### 🔧 Steps:
- Loaded and standardized the Iris dataset  
- Applied PCA with `n_components=2`  
- Visualized 2D projection colored by species  
- Calculated explained variance of first two PCs  
- Re-ran PCA with all components:
  - Bar plot of explained variance ratio  
  - Step plot of cumulative explained variance

### 📌 Insight:
- Two PCs preserve most variance and reveal class separation  
- Setosa class is clearly separable in reduced space  
- Cumulative plot helps decide how many PCs to retain

---

## 🧊 Bonus — PCA in 3D with Synthetic 4D Data

**Goal:** Practice PCA visualization in higher dimensions.

### 🔧 Steps:
- Created synthetic 4D data  
- Applied PCA with `n_components=3`  
- Visualized PCA-transformed data in 3D:
  - Matplotlib scatter with quivers  
  - Plotly interactive 3D scatter with PC vectors

### 📌 Insight:
- 3D PCA helps intuitively grasp variance distribution  
- Interactive plots enhance understanding of clustering

---

## 📊 Tools & Libraries

```python
numpy, matplotlib, sklearn (PCA, datasets, StandardScaler), plotly
