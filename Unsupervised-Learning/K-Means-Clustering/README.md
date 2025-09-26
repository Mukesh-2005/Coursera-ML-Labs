# 📊 Customer Segmentation with K-Means Clustering

This project applies **K-Means clustering** to segment customers based on demographic and behavioral data. The goal is to uncover meaningful customer groups that can help businesses tailor marketing strategies and improve customer retention.


## 🧠 Introduction to K-Means

**K-Means** is a popular unsupervised learning algorithm used to discover patterns in unlabeled data. It partitions data into **k clusters** based on feature similarity.

## Real-world applications include:

- Customer segmentation  
- Website behavior analysis  
- Pattern recognition  
- Feature engineering  
- Data compression

## 🧪 Synthetic Data Experiment

We first tested K-Means on synthetic data using `make_blobs`:

```python
X, y = make_blobs(n_samples=5000, centers=[[4,4], [-2, -1], [2, -3], [1, 1]], cluster_std=0.9)
```

Explored clustering with different values of k (3, 4, 5) to understand how cluster count affects grouping.

## 📦 Real-World Dataset

- Source: Customer Segmentation Dataset
- Rows after cleaning: 700 (from original 849)
- For this data set we use set the value of k = 3 
- Clustering Method:
```python
clusterNum = 3
k_means = KMeans(init='k-means++', n_clusters=clusterNum, n_init=12)
k_means.fit(X)
labels = k_means.labels_
```
## 📊 Insights from Clustering
Based on the clustering output and visual analysis (2D and 3D), the customers were grouped into:
- LATE CAREER, AFFLUENT, AND EDUCATED
- MID CAREER AND MIDDLE INCOME
- EARLY CAREER AND LOW INCOME
These segments can help businesses target high-value customers and optimize marketing efforts

## 📚 Learnings
- K-Means is effective for discovering hidden patterns in customer data
- Choosing the right number of clusters is key to meaningful segmentation
- 3D plots offer deeper insight into multi-feature clustering (though not shared here)



