# 📊 Customer Segmentation Using Clustering Algorithms
This project explores customer segmentation using five clustering techniques: K-Means, K-Prototypes, Hierarchical Clustering, DBSCAN, and Gaussian Mixture Models (GMM). 
The aim is to identify meaningful customer groups based on demographic, behavioral, and transactional data to support business decision-making and personalized marketing strategies.

--- 
# 📘 Project Overview

The dataset contains mixed numerical and categorical customer information. To ensure reliable segmentation, this project evaluates multiple clustering algorithms using:

- Quantitative Metrics

- PCA (Principal Component Analysis)

- t-SNE (Non-linear Visualization)

This comprehensive approach allows us to confirm whether clusters are meaningful and stable across different perspectives.

---

# 📂 Dataset Description
This data set contains 5,000 observatisons and 18 features.

Key features include:

- Demographics: Age, Gender, City

- Transaction Details: Unit Price, Quantity, Discount, Total Amount, Payment Method, Product Category

- Behavioral Data: Device Type, Pages Viewed, Session Duration

- Customer Experience: Delivery Time, Customer Rating

---

# 🛠️ Clustering Methods
1. **K-Means**

- Distance-based algorithm

- Works well with scaled numeric features

- Produces clear separation in PCA visualizations

2. **K-Prototypes**

- Designed for mixed (numerical + categorical) data

- Combines K-Means (numerical) and K-Modes (categorical)

- Shows strongest separation in t-SNE visualizations

3. **Hierarchical Clustering**

- Reveals a structure similar to K-Means

- Confirms the stability of a two-cluster solution

4. **DBSCAN**

- Density-based model

- Identifies only a few core samples

- Labels most data as noise → unsuitable for this dataset

5. **Gaussian Mixture Model (GMM)**

- Assumes clusters follow Gaussian distributions

- Produces heavily overlapping clusters

- Weak performance in both numeric metrics and visualizations

---
# 📈 Evaluation Metrics

Each model was evaluated using:

- Silhouette Score (↑ better)

- Calinski–Harabasz Score (↑ better)

- Davies–Bouldin Score (↓ better)

- Number of clusters formed

---

# 📋Result Summary

  | Clustering Method | Silhouette Score ↑ | Calinski–Harabasz ↑ | Davies–Bouldin ↓ | Number of Clusters |
|-------------------|---------------------|-----------------------|-------------------|----------------------|
| DBSCAN            | **0.6854**          | 109.3739              | **0.3792**        | 5                    |
| K-Prototypes      | 0.4170              | **683.6980**          | 1.4378            | 2                    |
| K-Means           | 0.3610              | 665.0806              | 1.6537            | 2                    |
| Hierarchical      | 0.3494              | **722.2351**          | 1.7916            | 2                    |
| GMM               | 0.1039              | 406.5712              | 3.2360            | 2                    |

---

# 🎨 PCA Visualizations

PCA plots show linear structure:

- K-Means, K-Prototypes, and Hierarchical models show clear separation along PC1

- GMM lacks defined separation and clusters overlap

- DBSCAN produces scattered points only (due to noise removal)

PCA confirms a two-cluster structure in the data.

---

# 🌈 t-SNE Visualizations

t-SNE reveals non-linear structure:

- K-Prototypes displays the best separation, forming compact and meaningful clusters

- K-Means and Hierarchical show moderate mixing, but still identifiable shapes

- GMM again collapses with heavy overlap

- DBSCAN detects only a small number of points

- t-SNE validates the superiority of mixed-type clustering for this dataset.

---
# 🧠 Final Conclusion

Although DBSCAN appears to score highest in Silhouette, it is not meaningful because it identified only a tiny set of core points. When considering all metrics, PCA, t-SNE, and interpretability, the most reliable clustering method is:

🎯 K-Prototypes (K = 2)

This model:

- Handles mixed categorical and numerical data

- Provides strong separation in t-SNE

- Shows stable structure in PCA

- Produces two clear, meaningful customer segments

K-Means and Hierarchical also perform well and validate the two-cluster structure.DBSCAN and GMM are not appropriate for this dataset.

--- 
# ⚙️ Technologies & Libraries Used

This project was built using Python and a collection of powerful data science and machine learning libraries:

- Python, Jupyter Notebook

- pandas, numpy, sqlite3, os, warnings

- matplotlib, seaborn, matplotlib.ticker

- scikit-learn:

  - KMeans, DBSCAN, GaussianMixture

  - StandardScaler, OneHotEncoder

  - ColumnTransformer, Pipeline

  - PCA, TSNE

  - silhouette_score, calinski_harabasz_score, davies_bouldin_score

  - NearestNeighbors

- K-Prototypes (kmodes.kprototypes)

- Hierarchical Clustering (scipy.cluster.hierarchy)

- kagglehub (for dataset access)
