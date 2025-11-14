📊 #Customer Segmentation Using Clustering Algorithms
This project explores customer segmentation using five clustering techniques: K-Means, K-Prototypes, Hierarchical Clustering, DBSCAN, and Gaussian Mixture Models (GMM). 
The aim is to identify meaningful customer groups based on demographic, behavioral, and transactional data to support business decision-making and personalized marketing strategies.

--- 
📘 **Project Overview**

The dataset contains mixed numerical and categorical customer information. To ensure reliable segmentation, this project evaluates multiple clustering algorithms using:

- Quantitative Metrics

- PCA (Principal Component Analysis)

- t-SNE (Non-linear Visualization)

This comprehensive approach allows us to confirm whether clusters are meaningful and stable across different perspectives.

---

📂 **Dataset Description**
This data set contains 5,000 observatisons and 18 features.

Key features include:

-Demographics: Age, Gender, City

- Transaction Details: Unit Price, Quantity, Discount, Total Amount, Payment Method, Product Category

- Behavioral Data: Device Type, Pages Viewed, Session Duration

- Customer Experience: Delivery Time, Customer Rating

---

🛠️ **Clustering Methods**
1. K-Means

- Distance-based algorithm

- Works well with scaled numeric features

- Produces clear separation in PCA visualizations

2. K-Prototypes

- Designed for mixed (numerical + categorical) data

- Combines K-Means (numerical) and K-Modes (categorical)

- Shows strongest separation in t-SNE visualizations

3. Hierarchical Clustering

- Reveals a structure similar to K-Means

- Confirms the stability of a two-cluster solution

4. DBSCAN

- Density-based model

- Identifies only a few core samples

- Labels most data as noise → unsuitable for this dataset

5. Gaussian Mixture Model (GMM)

- Assumes clusters follow Gaussian distributions

- Produces heavily overlapping clusters

- Weak performance in both numeric metrics and visualizations

---
📈 **Evaluation Metrics**

Each model was evaluated using:

- Silhouette Score (↑ better)

- Calinski–Harabasz Score (↑ better)

- Davies–Bouldin Score (↓ better)

- Number of clusters formed
