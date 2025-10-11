# 🗺️ Museum Clustering Across Canada — Unsupervised Learning with DBSCAN & HDBSCAN

This project explores the geographic distribution of museums across Canada using unsupervised machine learning techniques. By applying clustering algorithms to latitude and longitude data, we uncover regional patterns, identify dense cultural hubs, and compare the performance of DBSCAN and HDBSCAN.

---

## 📌 Project Goals

- Visualize the spatial distribution of museums across Canada
- Apply **DBSCAN** and **HDBSCAN** to identify clusters based on proximity
- Compare clustering performance and interpret results
- Practice geospatial preprocessing, scaling, and visualization

---

## 🧠 Algorithms Used

### DBSCAN
- Density-based clustering using fixed radius (`eps`) and minimum neighbors (`min_samples`)
- Performed well due to uniform density and manual coordinate scaling
- Result: **33 clusters**, **79 noise points**

### HDBSCAN
- Hierarchical clustering that adapts to varying densities
- More sensitive, produced many small clusters and labeled more points as noise
- Result: **145 clusters**, **458 noise points**

---

## 🗺️ Visualization

- Plots generated using **GeoPandas**, **Matplotlib**, and **Contextily**
- Basemaps overlaid to show geographic context
- Clusters color-coded for clarity
- Noise points highlighted separately

---

## 📊 Key Insights

- DBSCAN produced cleaner, more interpretable clusters for this dataset
- Manual scaling of latitude improved clustering balance
- HDBSCAN is powerful but requires careful tuning for geographic data
- Clustering reveals cultural density in cities like Toronto, Montreal, Vancouver

---

## 📈 Learning Outcome
This project was a big step in my unsupervised learning journey. I didn’t just run clustering algorithms — I learned how to think through them.
- At first, I was confused why my plots weren’t showing. Turns out, I needed to set up the plotting environment properly and match the coordinate systems. That small fix taught me a lot about geospatial visualization.
- I also wondered whether I should scale latitude and longitude. I tried StandardScaler, but it didn’t feel right. Then I realized — latitude and longitude have natural ranges, so I manually scaled latitude to balance the influence. That decision made DBSCAN perform much better.
- I kept asking myself: “Should I split the data into train and test sets?” But I learned that in unsupervised learning, especially clustering, we usually use the full dataset because there are no labels to predict.
- When I compared DBSCAN and HDBSCAN, I expected HDBSCAN to be smarter. But it gave me 145 clusters and labeled 458 museums as noise — way more than DBSCAN. That’s when I realized: HDBSCAN is powerful, but it’s also sensitive. DBSCAN gave me cleaner, more interpretable clusters for this dataset.
This wasn’t just about code — it was about learning how algorithms behave, how data structure matters, and how small decisions (like scaling) can change everything.



