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

**Join the Interactive Quiz on Slido**: [Slido Link](TBD)

