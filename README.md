# 💳 Customer Segmentation using K-Means and Hierarchical Clustering

This project focuses on **unsupervised learning** to identify distinct customer segments based on demographic and financial attributes.  
By leveraging **K-Means** and **Hierarchical Clustering**, this project aims to uncover meaningful customer groups that can support data-driven marketing and decision-making strategies.

---

## 📁 Project Overview
Customer segmentation is a key task in customer analytics, helping businesses understand their customer base and tailor personalized strategies.  
In this project, clustering algorithms are applied on a **customer dataset (`data_nasabah.csv`)**, which contains attributes such as:

- Gender  
- Education Level  
- Marital Status  
- Age  
- Income  
- Card Category  

The goal is to discover underlying **patterns or groups of customers** that exhibit similar behaviors and characteristics.

---

## 🧩 Objectives
- Preprocess and clean customer data for clustering.  
- Apply **Principal Component Analysis (PCA)** for dimensionality reduction.  
- Implement and evaluate **K-Means** and **Agglomerative (Hierarchical) Clustering**.  
- Compare clustering quality using silhouette, Davies–Bouldin, and Calinski–Harabasz metrics.  
- Visualize the resulting clusters for interpretation.

---

## 🛠️ Tools & Libraries
- **Python 3.8+**
- **Pandas**, **NumPy**
- **Matplotlib**, **Seaborn**
- **Scikit-learn**
- **Yellowbrick** (for Elbow method visualization)
- **Missingno**
- **PCA** for feature reduction

---

## ⚙️ Workflow

### 1. **Data Preprocessing**
- Handle missing values using `SimpleImputer` (mean and most frequent strategy).  
- Remove irrelevant columns (`ID_Nasabah`).  
- Normalize and scale numerical features using `StandardScaler` and `MinMaxScaler`.  
- Encode categorical features using `OrdinalEncoder` and `OneHotEncoder`.  

### 2. **Dimensionality Reduction**
- Apply **Principal Component Analysis (PCA)** to project features into 2D space for easier visualization and clustering.

### 3. **K-Means Clustering**
- Evaluate different numbers of clusters (k = 2–9) using:
  - **Elbow Method** (WCSS)
  - **Silhouette Score**
- Choose the optimal cluster count based on the best silhouette value and the elbow curve.

### 4. **Hierarchical Clustering**
- Use **Agglomerative Clustering** with multiple linkage methods (`ward`, `complete`, `average`, `single`).
- Compare silhouette scores across methods to find the best-performing linkage type.
- Visualize clustering results and centroids.

### 5. **Evaluation Metrics**
- **Silhouette Score** → Measures how well samples are clustered (higher is better).  
- **Davies–Bouldin Index** → Measures cluster separation (lower is better).  
- **Calinski–Harabasz Index** → Measures variance ratio between and within clusters (higher is better).  

---

## 📈 Results

### 🔹 Clustering Evaluation Summary

| Model / Method | Optimal Cluster | Silhouette Score ↑ | Davies–Bouldin ↓ | Calinski–Harabasz ↑ | Notes |
|-----------------|----------------|--------------------|------------------|----------------------|--------|
| **K-Means (k=2)** | 2 | **0.8529** | **0.2569** | **10002.76** | Excellent separation and cohesion |
| K-Means (k=3)** | 3 | 0.8300 | – | – | Slightly lower cohesion |
| **Agglomerative Clustering (Complete Linkage, k=2)** | 2 | **0.8533** | – | – | Comparable performance to K-Means |

**Interpretation:**
- Both **K-Means** and **Agglomerative Clustering** achieved strong clustering quality, with silhouette scores around **0.85**, indicating well-separated and cohesive clusters.  
- **K-Means** provided more compact clusters, while **Agglomerative Clustering** offered better interpretability through its hierarchical structure.  
- **Optimal number of clusters: 2**

---

## 📊 Visualization Examples

- **Silhouette Score vs Number of Clusters**
  Displays how clustering quality changes with different cluster counts.
- **Elbow Method (WCSS Curve)**
  Helps identify the optimal `k` value for K-Means.
- **Cluster Scatter Plot**
  Visualizes customer groups and their centroids after PCA reduction.

---

## 💡 Key Insights
- Two major customer segments were identified, each with distinct financial and demographic characteristics.  
- PCA successfully reduced data dimensionality while preserving key variance for clustering.  
- K-Means was more computationally efficient, whereas Agglomerative Clustering allowed for more interpretable hierarchical segmentation.  
- The clustering results can be used for targeted marketing, customer retention, and personalized offers.

---
