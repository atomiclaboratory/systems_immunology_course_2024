# Navigating High-Dimensional Data: Visualizing Patterns with t-SNE 🗺️🔬
**Team 1 - Jonas Salk**

---

### 👥 Team Members
- Electra Scarpignato
- Kara Walp
- Evan Horvath
- Ethan Masters

Team Salk will present advanced techniques for visualizing high-dimensional immunological data, focusing on **t-distributed Stochastic Neighbor Embedding (t-SNE)**. t-SNE is a powerful tool that reduces high-dimensional data into a lower-dimensional space suitable for visualization, enabling us to uncover complex patterns and relationships that are not apparent in raw data. They will also briefly introduce **Uniform Manifold Approximation and Projection (UMAP)** as another method for dimensionality reduction and visualization.

---

## 🌟 Class Activities

1. **Introduction to High-Dimensional Visualization (Until 4:00 PM) 🧠**
   - Overview of visualization techniques for high-dimensional data: t-SNE and UMAP.
   - Focus on understanding how t-SNE works, its applications, strengths, and limitations.
   - Discuss key differences between t-SNE, clustering methods (Team Margulis), and PCA (Team Brenner).

2. **Hands-on t-SNE Application with PANDORA (4:00 PM - 5:15 PM) 💻**
   - Practical application of t-SNE on immunological datasets using **PANDORA**.
   - **Task**: Apply t-SNE to visualize complex immune response data and interpret the clusters formed.
   - **Goal**: Discover hidden structures and patterns in high-dimensional immunological data by effectively visualizing it in two or three dimensions.

---

## 🧩 Concepts to Understand

### t-Distributed Stochastic Neighbor Embedding (t-SNE) 🗺️
t-SNE is a non-linear dimensionality reduction technique particularly well-suited for embedding high-dimensional data into a space of two or three dimensions, which can then be visualized in a scatter plot. It focuses on preserving local structure in data, making it excellent for visualizing clusters and patterns.

#### Key Features of t-SNE:
- **Local Structure Preservation**: Maintains the neighborhood relations of data points, ensuring similar points stay close in the reduced space.
- **Non-Linear Reduction**: Captures complex patterns that linear methods like PCA might miss.
- **Visualization**: Produces visually interpretable maps that can reveal hidden structures in data.
- **Comparison with PCA and Clustering**:
  - **PCA (Team Brenner)**: A linear method that focuses on capturing global variance.
  - **Clustering (Team Margulis)**: Groups data based on similarity but doesn't inherently reduce dimensions for visualization.
  - **t-SNE**: Balances between capturing local and some global structures, tailored for visualization rather than explicit data reduction.

---

## t-SNE Analysis in PANDORA: Step-by-Step 🚀

### Step 1: Data Selection 📂
- **Columns**: Leave empty to include all columns in the analysis.
- **Exclude**: Exclude `days_pso` from the dataset.
- **Grouping Variables**: Set `timepoint` and `disease severity` as grouping variables.

### Step 2: Preprocessing Steps 🧹
- Apply the following preprocessing settings:
  - **Center/Scale**: 📏 Standardize the data to ensure all variables contribute equally.
  - **MedianImpute**: 🩹 Handle missing values by imputing with the median.
  - **Correlation Filter (corr)**: 🔗 Remove variables with high correlation to reduce redundancy.
  - **Zero and Near-Zero Variance Filter (zv/nzv)**: ⚙️ Exclude variables with little to no variability.

### Step 3: Clustering Settings 🔍
- Use **Mclust (DBSCAN)** for clustering:
  - **DBSCAN**: A density-based clustering algorithm that groups points based on their proximity and marks outliers.
  - **epsQuantile**: Sets the distance threshold to define clusters; higher values create broader clusters, and lower values tighten clustering.
- Set the `epsQuantile` parameter to `1`.
- Set the number of cluster groups to `3`.

### Step 4: t-SNE Settings ⚙️
- **Perplexity**: Test values `5`, `20`, `30`, `50`, and `100`.
  - *Defines the balance between local and global structure in the data. Lower values focus on local details, while higher values capture broader structures.*
- **Exaggeration Factor**: Test values `4`, `12`, `36`, and `100`.
  - *Controls the spread of points during the embedding process. Higher values exaggerate separations between clusters.*
- **Max Iterations**: Test values `250`, `1,000`, and `10,000` with a fixed learning rate of `500`.
  - *Sets the number of optimization steps; higher values increase precision but take longer.*
- **Learning Rate (eta)**: Test values `10`, `30`, and `500` with max iterations fixed at `10,000`.
  - *Determines the step size during optimization. A low value slows down convergence, while a high value can destabilize results.*

### Step 5: Plot and Analyze 📊
- Run the analysis by clicking **PLOT IMAGE** and observe the t-SNE plot.
- Use the color-coded grouping variables (`timepoint` and `disease severity`) to interpret clusters.

---

## 📊 Interpreting t-SNE Results

Understanding the t-SNE output involves examining how data points are arranged in the reduced-dimensional space:

### 1. **Cluster Formation**
- **Interpretation of Clusters**: Groups of data points that cluster together may share similar immunological profiles.
- **Separation of Clusters**: Distinct clusters indicate significant differences in the underlying data, potentially correlating with biological variables like disease severity.

### 2. **Color-Coding and Patterns**
- **Grouping Variables**: By color-coding data points, you can observe how different categories distribute across the visualization.
- **Identifying Trends**: Patterns in color distribution can reveal relationships between immunological features and clinical outcomes.

---

## 🎯 Team Task

### Research Questions

**Visualizing Immune Response Patterns Associated with Disease Severity**

To explore how high-dimensional immunological data can be visualized to reveal patterns associated with disease severity in SARS-CoV-2 infections, we will perform t-SNE analysis on the entire COVID19-PITCH dataset. Our main objectives are:

1. **Hypothesis**: t-SNE visualization will reveal distinct clusters corresponding to different disease severities, uncovering subtle differences in immune responses.
2. **Objective**: Use t-SNE to reduce the dimensionality of immunological parameters and visualize how samples group based on disease severity.
3. **Analysis Goal**: Identify whether t-SNE can effectively separate asymptomatic, mild, and severe cases, and determine which immunological features contribute to these separations.

**Join the Interactive Quiz on Slido**: [Slido Link](https://app.sli.do/event/cTfKSL3Dq2sHKMnfSArQMo)

---

# Quiz Questions for t-SNE Analysis

## Correct Answers

1. **What is the primary goal of t-SNE in unsupervised machine learning?**  
   **Correct Answer:** To reduce high-dimensional data into a lower-dimensional space for visualization.

2. **In the context of t-SNE, what does a perplexity value represent?**  
   **Correct Answer:** The expected number of nearest neighbors around each data point.

3. **Based on the results, which perplexity value yielded the most efficient grouping of data in this dataset?**  
   **Correct Answer:** A perplexity value of 30 yielded the most efficient grouping of data.

4. **What is the primary drawback of choosing a perplexity value of 100 in t-SNE analysis?**  
   **Correct Answer:** It merges clusters, failing to segment the data properly.

5. **Why is it important to analyze multiple t-SNE plots with different perplexity values?**  
   **Correct Answer:** To ensure the global geometry and local density relationships are properly balanced.

6. **How does exaggeration factor influence the results of t-SNE on this dataset?**  
   **Correct Answer:** It controls the spacing between clusters but has minimal effect.

7. **What is the optimal number of iterations for this dataset when the learning rate is set to 500?**  
   **Correct Answer:** The optimal number of iterations is 1,000.

8. **Is the learning rate important for this dataset when using t-SNE?**  
   **Correct Answer:** No, the results were consistent across all tested learning rates, indicating no significant effect.

9. **In a t-SNE plot, what can you infer if two clusters appear to be the same size?**  
   **Correct Answer:** t-SNE expands dense clusters and contracts sparse ones, making cluster sizes appear similar.

10. **Why does the t-SNE plot change each time you adjust hyperparameters?**  
    **Correct Answer:** t-SNE uses random initialization, and small changes in hyperparameters can lead to different optimization paths, affecting the outcome.

11. **When analyzing distances between clusters in a t-SNE plot, what do you need to consider?**  
    **Correct Answer:** The distances between clusters may not represent true relationships in the original high-dimensional space due to non-linear transformations.

12. **If one cluster consists exclusively of asymptomatic individuals, what does this suggest?**  
    **Correct Answer:** The absence of clinical signs and measurements in asymptomatic individuals resulted in their distinct separation based on the lack of these variables.

13. **Considering both the immunological variables and clinical symptoms for Cluster 1, what does this profile indicate about the individuals in this group?**  
    **Correct Answer:** The combination of strong immune activation and systemic symptoms in Cluster 1 aligns these individuals more closely with profiles observed in severe cases, despite their mild classification.

14. **Beyond immunological data, which of the following demonstrates the versatility of t-SNE and unsupervised machine learning in high-dimensional data analysis?**  
    **Correct Answer:** Identifying latent cell states and heterogeneity within large-scale single-cell transcriptomic datasets without prior assumptions.

---

## 🎉 Quiz Winners
![Quiz Winners](https://github.com/atomiclaboratory/systems_immunology_course_2024/blob/main/Course%20Materials/MODULE%204%20-%20Weeks%207-14/team%201%20Jonas%20Salk/images/tSNE-%20quiz%20winners.png)

---

## 📚 Additional Reading Materials on t-SNE

### Articles and Blogs
- [Exploring t-SNE](http://nickc1.github.io/dimensionality/reduction/2017/11/04/exploring-tsne.html) - A great introductory blog post to understand t-SNE and its applications.

- [Understanding t-SNE and Its Pitfalls](https://distill.pub/2016/misread-tsne/) - A comprehensive guide to interpreting t-SNE plots and avoiding common misinterpretations.

### Videos
- [Google t-SNE Introduction (3 min)](https://www.youtube.com/watch?v=wvsE8jm1GzE) - A short and engaging video explaining the basics of t-SNE.
  
- [StatQuest: t-SNE (12 min)](https://www.youtube.com/watch?v=NEaUSP4YerM) - A detailed and easy-to-follow explanation of t-SNE with visual aids.

### Academic Paper
- [Original t-SNE Paper by van der Maaten and Hinton](https://lvdmaaten.github.io/publications/papers/JMLR_2008.pdf) - The foundational research paper introducing t-SNE, covering the algorithm and its mathematical foundation.
