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

## t-SNE Analysis in PANDORA

### Step 1: Data Selection
- **Choose Data Columns**: Select the high-dimensional features you wish to visualize. This could include various immunological parameters like cell counts, cytokine levels, etc.
- **Default Setting**: If no specific columns are selected, PANDORA will include all valid numerical columns.

### Step 2: Preprocessing Options
- **Standardization**: Apply `Center/Scale` to normalize your data, ensuring each feature contributes equally to the analysis.
- **Handling Missing Values**: Use `MedianImpute` to fill in any missing data points, which helps in maintaining the integrity of the dataset.

### Step 3: t-SNE Settings
- **Perplexity**: Set the perplexity parameter (commonly between 5 and 50). This balances attention between local and global aspects of your data.
- **Learning Rate**: Adjust the learning rate to control how the algorithm converges.
- **Iterations**: Specify the number of iterations for optimization (a higher number can lead to more stable results).

### Step 4: Grouping Variables
- **Color Coding**: Choose a categorical variable to color-code your data points, such as disease severity or time points.
  - **Example**: Select "Disease Severity" to observe how different severity levels cluster in the visualization.

### Step 5: Display Options
- **Plot Customization**: Adjust font sizes, point sizes, and other visual aspects for clarity.

After configuring these settings, **click PLOT IMAGE** to run the t-SNE analysis.

---

## 📊 Interpreting t-SNE Results

Understanding the t-SNE output involves examining how data points are arranged in the reduced-dimensional space:

### 1. **Cluster Formation**
- **Interpretation of Clusters**: Groups of data points that cluster together may share similar immunological profiles.
- **Separation of Clusters**: Distinct clusters indicate significant differences in the underlying data, potentially correlating with biological variables like disease severity.

### 2. **Color-Coding and Patterns**
- **Grouping Variables**: By color-coding data points, you can observe how different categories distribute across the visualization.
- **Identifying Trends**: Patterns in color distribution can reveal relationships between immunological features and clinical outcomes.

### 3. **Analyzing Outliers**
- **Outlier Detection**: Data points that are isolated from clusters may represent unique cases or anomalies in the dataset.
- **Investigate Further**: Outliers should be examined to determine if they are due to data errors or represent significant biological variations.

---

## 🎯 Team Task

### Research Questions

**Visualizing Immune Response Patterns Associated with Disease Severity**

To explore how high-dimensional immunological data can be visualized to reveal patterns associated with disease severity in SARS-CoV-2 infections, we will perform t-SNE analysis on the entire COVID19-PITCH dataset. Our main objectives are:

1. **Hypothesis**: t-SNE visualization will reveal distinct clusters corresponding to different disease severities, uncovering subtle differences in immune responses.
2. **Objective**: Use t-SNE to reduce the dimensionality of immunological parameters and visualize how samples group based on disease severity.
3. **Analysis Goal**: Identify whether t-SNE can effectively separate asymptomatic, mild, and severe cases, and determine which immunological features contribute to these separations.

**Join the Interactive Quiz on Slido**: [Slido Link](TBD)

