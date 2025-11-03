# 🧪 Dimensionality Reduction Lab: t-SNE vs UMAP vs PCA

## 🎯 Objective
To compare three popular dimensionality reduction techniques — **t-SNE**, **UMAP**, and **PCA** — on a synthetic 3D dataset. The goal is to evaluate how well each method preserves cluster structure in terms of separation, density, and relative distances.

---

## 📁 Dataset
- **Type**: Synthetic 3D blobs
- **Samples**: 500
- **Clusters**: 4
- **Centers**: [[2, -6, -6], [-1, 9, 4], [-8, 7, 2], [4, 7, 9]]
- **Standard deviations**: `[1, 1, 2, 3.5]`

---

## 🧰 Tools & Libraries
- `numpy`, `pandas`, `matplotlib`, `plotly`
- `sklearn`: `make_blobs`, `StandardScaler`, `TSNE`, `PCA`
- `umap`: `UMAP`

---

## 🔄 Workflow Summary

### 1. Data Generation
- Created synthetic blobs with varied spread.
- Stored true labels for evaluation.

### 2. 3D Visualization
- Used `plotly.express.scatter_3d` for interactive inspection of cluster density and overlap.

### 3. Standardization
- Applied `StandardScaler()` to normalize features before projection.

### 4. Dimensionality Reduction

| Method | Parameters | Key Observations |
|--------|------------|------------------|
| **t-SNE** | `perplexity=30`, `max_iter=1000` | Strong cluster separation, good local structure, some global distortion. |
| **UMAP** | `min_dist=0.5`, `spread=1` | Balanced local/global structure, preserved continuity between overlapping clusters. |
| **PCA** | `n_components=2` | Fastest; preserved variance and relative distances well despite being linear. |

---

## 📊 Outputs

- ✅ Interactive 3D plot of original blobs
- ✅ 2D scatter plots for:
- t-SNE projection
- UMAP projection
- PCA projection
- ✅ Text cells with observations and interpretation prompts

---

## 🧠 Comparative Summary

| Method | Strengths | Weaknesses |
|--------|-----------|------------|
| **t-SNE** | Excellent local clustering; visually distinct clusters | Global distances may be misleading; sensitive to hyperparameters |
| **UMAP** | Balances local/global structure; preserves continuity | Sensitive to `n_neighbors`, `min_dist`; results can vary |
| **PCA** | Fast, interpretable, preserves variance | Can’t capture non-linear structure |

📌 In this experiment:
- **PCA** was surprisingly effective and fast.
- **t-SNE** gave strong separation.
- **UMAP** offered a more connected, interpretable view of overlapping clusters.

---

## 🔬 Suggested Next Steps

- ✅ Run all cells to capture final plots and numerical outputs.
- 🔧 Tune hyperparameters:
- t-SNE: Try `perplexity` from 5 to 50, adjust `early_exaggeration`.
- UMAP: Experiment with `n_neighbors`, `min_dist`, `spread`.
- 📈 Quantify embeddings:
- Use **Silhouette Score**, **Adjusted Rand Index**, or **Trustworthiness**.
- 💾 Save visuals and scripts:
- Export best plots and document findings.
- Create a reproducible script with tuned parameters.

---

## 🗣️ Reflections
This lab helped me understand how different dimensionality reduction techniques behave on clustered data. I learned how to interpret 2D projections, tune hyperparameters, and evaluate embeddings both visually and quantitatively.

---
>Built by Mukesh — part of my unsupervised learning series
>📅 Last updated: November 2025
