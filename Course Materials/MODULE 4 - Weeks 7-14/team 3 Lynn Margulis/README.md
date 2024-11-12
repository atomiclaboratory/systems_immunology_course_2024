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
   - Task: Use HClust to stratify individuals into N-IgG high and low responders based on serological responses to SARS-CoV-2 infection.

---

## 🧩 Concepts to Understand

### Hierarchical Clustering (HClust) 🔍
Hierarchical Clustering (HClust) is an unsupervised learning technique that groups data points based on their similarities, visualized through a **dendrogram**. Dendrogram is built by successively merging or splitting clusters based on distance, useful for identifying nested cluster structures. Different **distance measures** and **linkage methods** influence how clusters are formed, each with unique characteristics useful for specific data types and clustering goals.

#### Key Features of HClust:
- **Dendrogram Structure**: Visualizes the merging process of clusters, showing relationships and nested structures in the data.
- **Distance Measure**: Used to calculate dissimilarities among samples, providing a basis for grouping.
- **Linkage Method**: Applied for merging, which minimizes the variance within clusters, forming tighter and more cohesive clusters.

#### Distance Measures
1. **Correlation**: Measures the similarity between two data points based on the correlation coefficient, indicating how variables move in relation to each other.
2. **Euclidean**: Calculates the straight-line distance between points in multidimensional space. Commonly used, it captures overall similarity based on magnitude.
3. **Maximum**: Also known as Chebyshev distance, it considers the maximum difference between dimensions of two points, highlighting the largest deviation.
4. **Manhattan**: Computes distance based on absolute differences across dimensions, summing each dimension’s distance (like navigating a city grid).
5. **Canberra**: Emphasizes relative differences by dividing absolute differences by the sum of values for each dimension, making it sensitive to small values.
6. **Binary**: Compares data points based on binary attributes, often used for categorical data, counting mismatches (0 vs. 1) between points.
7. **Minkowski**: A generalized distance measure, extending Euclidean and Manhattan distances by varying the order parameter \( p \); for \( p = 2 \) it becomes Euclidean, and for \( p = 1 \) it becomes Manhattan.

#### Linkage Methods
1. **Single Linkage**: Connects clusters based on the smallest distance between any two points across clusters, often forming elongated clusters.
2. **Complete Linkage**: Uses the largest distance between points in clusters, resulting in compact, evenly shaped clusters.
3. **Average Linkage**: Calculates the average distance between all pairs of points in two clusters, balancing compactness and connectivity.
4. **McQuitty (WPGMA)**: Weighs clusters equally regardless of size, using the average of the minimum distances.
5. **Median Linkage**: Centers clusters around the median distance, which can help stabilize clusters but may not form balanced structures.
6. **Centroid Linkage**: Uses the centroids (mean points) of clusters for merging, often forming natural groupings based on the central location.
7. **Ward’s Method (Ward.D and Ward.D2)**: Minimizes the variance within clusters by choosing merges that produce the smallest increase in total within-cluster variance. **Ward.D2** is a variation that uses squared Euclidean distances, creating very tight, cohesive clusters.

In today's class, we’ll apply **Euclidean distance** with **Ward.D2 linkage** in HClust to capture immune response profiles and identify predictive clusters based on their early immunological characteristics.

#### How to Run HClust Analysis in PANDORA:
1. **Prepare the Data**: Use immunological parameters measured on day 28 post-symptom onset (pso).
2. **Compute Dissimilarity Matrix**: Calculate using **Euclidean distance** to capture similarities among samples.
3. **Cluster Formation**: Apply **Ward’s D2 linkage method** to join the most similar clusters iteratively.
4. **Plot the Dendrogram**: Visualize in a heatmap with the tightest clusters ordered first, revealing distinct groups (e.g., high and low responders).

---

## 🎯 Team Tasks

### TASK 1: Identify Predictive Immunological Signatures with HClust 🔄
- **Objective**: Use HClust to identify early immunological signatures that predict whether an individual will maintain a high-magnitude immune response six months after SARS-CoV-2 infection.
- **Goal**: Distinguish between high and low responders by analyzing clustering results and the corresponding immunological features on day 28 pso.

### 📝 Quiz for HClust Task:
**Join the Interactive Quiz on Slido**

**Quiz Questions**:
- **Q1**: What does the structure of a dendrogram tell us about the immune response data?
  - **Answer**: It shows relationships and nested clusters, helping identify distinct immune response groups.

- **Q2**: Why is the Ward’s D2 linkage method beneficial for clustering immunological data?
  - **Answer**: It minimizes variance within clusters, creating tighter, more interpretable groupings.

- **Q3**: Based on your HClust analysis, which immunological features on day 28 seem most predictive of a high response at 6 months?
  - **Answer**: Likely strong anti-N IgG titers and increased T cell responses, though results may vary.
