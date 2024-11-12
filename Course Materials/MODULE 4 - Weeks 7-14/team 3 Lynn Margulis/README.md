# Clustering Methods to Reveal Hidden Structures in Immune Response Data 🧩📊
**Team 3 - Lynn Margulis**

---

### 👥 Team Members
- Kaavya Akula
- Joseph Soto
- Marek Pinto
- Julia Nowak

Today, Team Margulis will present unsupervised clustering methods, including **K-means**, **Hierarchical Clustering (HClust)**, and **DBSCAN**, as powerful techniques to uncover hidden structures in immune response data. These methods allow us to group data points based on similarities without needing labeled outcomes, which is particularly useful for identifying patterns in complex immunological datasets.

---

## 🌟 Class Activities

1. **Introduction to Clustering Techniques (Until 4:00 PM) 🧠**
   - Overview of unsupervised clustering techniques: K-means, HClust, and DBSCAN.
   - Key focus on understanding how these methods help in grouping data points based on similarity, with examples relevant to immune response data.

2. **Hands-on Clustering Application with PANDORA (4:00 PM - 5:15 PM) 💻**
   - Practical application of clustering techniques on immunological datasets using **PANDORA**.
   - Emphasis on **Hierarchical Clustering (HClust)**, exploring how different dendrogram structures reveal immune response patterns.
   - Comparison between clustering methods to see which best reveals distinct groupings within the dataset.

---

## 📊 Dataset Overview
- We will be using the immunological dataset available in the 'Dataset' folder, similar to previous classes.

---

## 🧩 Concepts to Understand

### Clustering Techniques 🔍
Clustering is an unsupervised learning technique used to group data points based on their inherent similarities. In immunology, clustering can help us identify subgroups within immune responses that might correlate with certain outcomes, like high or low responder profiles.

- **K-means Clustering**: Partitions data into a set number of clusters, each represented by the cluster’s centroid.
- **Hierarchical Clustering (HClust)**: Builds a dendrogram by successively merging or splitting clusters based on distance, useful for identifying nested cluster structures.
- **DBSCAN (Density-Based Spatial Clustering of Applications with Noise)**: Groups data points based on density, useful for identifying clusters of varying shapes and sizes, including outliers.

---

## 🎯 Team Tasks

### TASK 1: Comparison of Clustering Methods 🔄
- **Objective**: Apply hierarchical clusterinh (HClust) to the dataset to identify distinct clusters within the immune response data.
- **Goal**: Determine which method best captures natural groupings and provides interpretable clusters.

### 📝 Quiz for Task 1:
**Join the Interactive Quiz on Slido**

**Before analysis**:
- **Q1**: Based on the characteristics of each clustering method, which one would you expect to perform best on the immune response dataset, and why?
- **Q2**: Why is it useful to use clustering in immunological data analysis?

**After analysis**:
- **Q1**: Which clustering method produced the most distinct and interpretable clusters, and why?
- **Q2**: Which method struggled the most with noise in the dataset, and why?

---

### TASK 2: Exploring Clustering Parameters 📊
- **Objective**: Test different parameters within each clustering method to see how they affect clustering results.
  - **K-means**: Experiment with different numbers of clusters (k values).
  - **HClust**: Experiment with different linkage methods (e.g., single, complete, average).
  - **DBSCAN**: Adjust parameters for neighborhood radius and minimum points per cluster.

### 📝 Quiz for Task 2
**Parameter Exploration**
- **Q1**: What effect does increasing the number of clusters (k) in K-means have on the cluster compactness?
- **Q2**: In HClust, how does the choice of linkage method impact the shape and interpretability of clusters?
- **Q3**: How does changing the neighborhood radius in DBSCAN affect cluster formation, especially in noisy data?

---

### TASK 3: Practical Application and Interpretation 🧪
- **Objective**: Use the best-performing clustering method(s) to identify biologically meaningful clusters in immune response data and interpret their implications.

### 📝 Quiz for Task 3:

- **Q1**: What insights can we gain from the clusters identified in the immune response data?
- **Q2**: How might these clusters help in stratifying patients or predicting immune responses?
- **Q3**: Which clustering method would you recommend for future analyses on similar datasets, and why?