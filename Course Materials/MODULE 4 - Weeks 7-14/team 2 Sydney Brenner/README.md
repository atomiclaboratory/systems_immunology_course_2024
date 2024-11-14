# Simplifying Complexity: Extracting Key Patterns in Immunological Data with PCA 🧬📉
**Team 2 - Sydney Brenner**

---

### 👥 Team Members
- Ziqing Yu
- Erica Anton
- Annelisa Fache
- Alex Norman

Today, Team Brenner will present dimensionality reduction techniques, focusing on **Principal Component Analysis (PCA)** as a powerful tool to simplify complex immunological datasets. PCA reduces dataset complexity while preserving essential information, enabling us to identify key patterns that reveal relationships and variations in immune responses.

---

## 🌟 Class Activities

1. **Introduction to Dimensionality Reduction (Until 4:00 PM) 🧠**
   - Overview of dimensionality reduction techniques: PCA and Multiple Correspondence Analysis (MCA).
   - Focus on understanding PCA, how it reduces the number of variables in data, and how it differs from clustering methods like those presented by Team Margulis.

2. **Hands-on PCA Application with PANDORA (4:00 PM - 5:15 PM) 💻**
   - Practical application of PCA on immunological datasets using **PANDORA**.
   - Task: Test and interpret the results of PCA to identify principal components that best capture variation in immune response data.
   - **Goal**: Determine how PCA can simplify complex datasets and highlight key immunological patterns while retaining the most critical information.

---

## 🧩 Concepts to Understand

### Principal Component Analysis (PCA) 📉
PCA is a dimensionality reduction technique that transforms high-dimensional data into a smaller set of uncorrelated components, called **principal components**. These components represent the directions in which data variation is highest, making it easier to interpret complex datasets by focusing on a few main axes of variation.

#### Key Features of PCA:
- **Principal Components**: New variables created from original data that capture the highest variance in the dataset.
- **Variance Explanation**: Each principal component explains a portion of the total dataset variance, allowing for the selection of components that retain meaningful information.
- **Interpretation**: Enables identification of patterns, relationships, and trends that may not be obvious in raw data.
- **Comparison with Clustering**: While PCA reduces dimensions based on variance, clustering groups data based on similarity, as seen in Team Margulis’s presentation.

---

## PCA Analysis in PANDORA
1. **Select Parameters**: Use immunological data such as antibody and T-cell responses measured across different days.
2. **Pre-processing Steps**: Normalize and scale the data (center/scale) to ensure that each variable contributes equally; and impute missing values with MedianImpute.
3. **Run PCA**: Execute PCA in PANDORA to extract the top principal components that explain the highest variance.
4. **Interpret Results**: Analyze the loadings of each variable on the principal components to understand which immune responses are most influential in driving variation in the data.
5. **Visualize**: Create plots to visualize clusters of data points along the principal components, helping to identify natural groupings or trends in immune responses.

---

## 🎯 Team Task

### TASK: Analyzing and Interpreting PCA Results 🔄
- **Objective**: Use PCA to uncover key patterns in the dataset, interpreting the meaning of each principal component and how it relates to immune response.
- **Goal**: Identify the principal components that capture the most significant variance, interpret the main factors driving these components, and reflect on the advantages of using PCA to analyze immunological data.

**Join the Interactive Quiz on Slido**: [Slido Link](https://app.sli.do/event/goiF4Knx2J2M5bHahCZ7XA)

**Quiz Questions**:
1. Which principal components explained the highest variance in immune response data?
2. How do we interpret the main components in relation to specific immune response variables?
3. What are the advantages of using PCA over clustering methods like HClust when exploring immune data?
4. How does PCA help in identifying which immune variables are most influential in driving variation in the dataset?
5. What are some limitations of PCA compared to clustering methods in terms of identifying distinct groups?