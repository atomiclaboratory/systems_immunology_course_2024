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
   - Practical application of HClust on immunological datasets using **PANDORA**.
   - Task: Test and compare 4 different clustering methods (Ward D2, single linkage, average linkage, and complete linkage) to see how each method affects the formation and visual clarity of clusters.
   - **Goal**: Determine which method best separates high and low responders based on specific immunological parameters.

---

## 🧩 Concepts to Understand

#### Hierarchical Clustering (HClust) 🔍
Hierarchical Clustering (HClust) is an unsupervised learning technique that groups data points based on their similarities, visualized through a **dendrogram**. Dendrogram is built by successively merging or splitting clusters based on distance, useful for identifying nested cluster structures. Different **distance measures** and **linkage methods** influence how clusters are formed, each with unique characteristics useful for specific data types and clustering goals.

#### Key Features of HClust:
- **Dendrogram Structure**: Visualizes the merging process of clusters, showing relationships and nested structures in the data.
- **Distance Measure**: Used to calculate dissimilarities among samples, providing a basis for grouping.
- **Linkage Method**: Applied for merging, which minimizes the variance within clusters, forming tighter and more cohesive clusters.
- **Grouping variables**: N IgG responder status and disease severity, used only for interpretation and not included in clustering.

---

## HClust Analysis in PANDORA
1. **Select Parameters**: Use immunological data such as antibody responses (e.g., anti-N IgG) and T cell proliferation measured on day 28 post infection.
2. **Choose Distance Measure**: Use **Euclidean distance** for this analysis to calculate similarity between individuals.
3. **Apply Clustering Method**: Run HClust using each of the following linkage methods:
   - **Ward D2**: Minimizes within-cluster variance for tighter, more cohesive clusters.
   - **Single Linkage**: Links clusters based on the closest data points; can lead to elongated clusters.
   - **Average Linkage**: Uses the average distance between points, balancing compactness and separation.
   - **Complete Linkage**: Links based on the farthest points, often maximizing separation but creating uneven cluster sizes.
4. **Interpret the Dendrogram**: Observe how different linkage methods impact cluster appearance and clarity in separating high vs. low responders.

---

## 🎯 Team Task

### TASK: Testing, Comparing, and Interpreting Clustering Methods 🔄
- **Objective**: Use each of the four linkage methods (Ward D2, single, average, complete) to analyze how clusters form and how well they separate high and low responders.
- **Goal**: Identify which method best reveals distinct responder profiles, interpret how grouping variables (e.g., N IgG responder status, disease severity) help explain clusters, and reflect on the advantages and limitations of using HClust in this exploratory analysis.

**Join the Interactive Quiz on Slido**: [Slido Link](https://app.sli.do/event/goiF4Knx2J2M5bHahCZ7XA)

**Quiz Questions**:
1. Which clustering method provided the clearest separation of high and low responders?
2. How does the appearance of the dendrogram differ between single and Ward D2 linkage, and which is more useful for distinct group separation?
3. How do we interpret high and low responder clusters in relation to N IgG responder status and disease severity?
4. Which grouping variable correlates most with high response levels in this dataset?
5. When is unsupervised ML, like HClust, more appropriate than supervised ML in immunology research?
6. What are the limitations of HClust compared to supervised methods in predicting immune outcomes?