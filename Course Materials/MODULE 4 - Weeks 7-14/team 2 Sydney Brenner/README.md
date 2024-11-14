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

### Step 1: Column Selection
- **Choose Columns**: Select specific columns you wish to analyze and plot. Leaving this empty will include all valid numerical columns, except excluded ones.
- **Default Setting**: If no columns are selected, PANDORA will automatically take the first `n` columns from your dataset, up to a maximum of 50,000.
- **Excluded Columns**: No excluded columns by default.

### Step 2: Preprocessing Options
- **Unique Threshold**: Removing columns with fewer than a defined number of unique values (default:5) helps eliminate variables that don’t provide enough variation, which could otherwise lead to misleading or insignificant components in the analysis.
- **OPTIONAL - Percentage Threshold**: Columns with unique values below 10% of the total observations lack variability, which can skew results or add noise to the PCA. By excluding these low-variability columns, we focus on variables that contribute more effectively to capturing the true patterns and variance in the dataset.
*These steps are necessary to ensure that PCA operates on meaningful variables!*
- **Percentage Threshold**: 
- **Preprocessing**: Use `MedianImpute` for handling missing values, and apply `Center/Scale` to standardize data across variables. This standardization ensures that all variables contribute equally to PCA, which is critical for meaningful results.
- **Remove NA Option**: Turn this on to remove NA values from grouping variables.

### Step 3: PCA Settings
- **Choose Grouping Variable**: Grouping variables are excluded from PCA calculations and preprocessing. They are used solely for plotting and displaying PCA results. Only variables with unique values less than 10% of total observations appear here.
   - **Example**: Select "Disease Severity" (with values asymptomatic, mild, severe) as the grouping variable.
   - **Research Question**: Investigate immunological parameters (B cells, T cells, SARS-CoV-2-specific T cells, antibody profiles) measured across 6 time points up to 6 months post-infection to analyze patterns related to disease severity.
- **Component Limits**: If there are more than 1000 columns, Bartlett’s test and the Kaiser-Meyer-Olkin measure will be skipped due to computational limitations.

### Step 4: Display Options
- **Font Size**: Set font size to 16 for clarity in the plots.

After configuring these settings, **click PLOT IMAGE** to initiate the PCA analysis.

---

## 📊 Interpreting PCA Results

Once the PCA is complete, understanding the output involves examining several key measures and plots:

### 1. **PCA Performance Checks**

- **🧪 Bartlett's Test of Sphericity**: Checks if the dataset is suitable for PCA by evaluating correlations among variables. A p-value > 0.05 suggests PCA may not be informative, while a low p-value supports its use.

- **🔎 Kaiser-Meyer-Olkin (KMO) Index**: Assesses sampling adequacy, with values from 0 to 1. A value >0.6 is considered acceptable, indicating sufficient shared variance for PCA.
         KMO ≥ 0.90: "Marvelous" – Excellent common variance, ideal for PCA.
         0.80 ≤ KMO < 0.90: "Meritorious" – Very good common variance, suitable for PCA.
         0.70 ≤ KMO < 0.80: "Middling" – Adequate common variance, PCA is generally appropriate.
         0.60 ≤ KMO < 0.70: "Mediocre" – Acceptable, but only marginally suitable for PCA.
         0.50 ≤ KMO < 0.60: "Miserable" – Poor common variance; PCA may not be appropriate.
         KMO < 0.50: "Unacceptable" – Very low common variance, unsuitable for PCA.

### 2. **Eigenvalues and Scree Plot**

- **🔢 Eigenvalues**: Represent the variance captured by each principal component (PC). PCs with higher eigenvalues explain more dataset variation. Typically, components with eigenvalues >1 are retained as they capture more variance than individual variables.

- **📉 Scree Plot**: Visualizes eigenvalues to help determine the optimal number of PCs. The “elbow” point, where the explained variance sharply decreases, suggests the number of PCs to retain.

### 3. **PCA Interpretation Plots**

- **🔗 Correlation Plot**: Shows relationships among variables based on their loading on each PC.
  - Variables close together are positively correlated, while those in opposite quadrants are negatively correlated.
  - Variables farther from the origin are better represented by the PCs.

- **📐 Cos² Plot (Squared Cosine)**: Reflects the quality of variable representation on the factor map. Higher cos² values indicate better representation by the PCs. 

- **🎯 Contribution Plot**: Displays each variable’s contribution percentage to the variance explained by specific PCs. Variables with high contributions on primary PCs are crucial in explaining data variability.

- **🔀 Biplot**: Combines sample and variable projections on PCs, illustrating which variables most influence sample positions. Observing patterns based on variables or groups can reveal clustering trends or relationships within the data.

---

## 🎯 Team Task

### Research Questions

**Integrative Analysis to Identify Immune Parameters Associated with Disease Severity**

To investigate the trajectory of cellular and humoral adaptive immune responses during SARS-CoV-2 infection and their relationship with disease severity, perform an integrative analysis on aggregated immunological data from 433 samples obtained from 86 donors (12 asymptomatic, 66 mild, 8 severe) at 6 different time points. Our main objectives are:

1. **Hypothesis**: Samples from asymptomatic individuals may resemble those taken at later time points from individuals with mild, symptomatic disease, suggesting a similarity in immune response evolution.
2. **Objective**: Identify immunological differences between individuals with asymptomatic and mild infections by performing PCA on immunological parameters alone.
3. **Analysis Goal**: Determine if immunological parameters alone can explain a significant portion of variance in SARS-CoV-2 positive individuals, revealing distinct immunophenotypes among asymptomatic, mild, and severe cases.

PCA will allow us to examine patterns in immune responses across disease severities, helping identify critical variables—such as specific T cell responses and antibody markers—that drive differences in immune profiles.

### TASK: Analyzing and Interpreting PCA Results 🔄
- **Objective**: Use PCA to uncover key patterns in the dataset, interpreting the meaning of each principal component and how it relates to immune response.
- **Goal**: Identify the principal components that capture the most significant variance, interpret the main factors driving these components, and reflect on the advantages of using PCA to analyze immunological data.

**Join the Interactive Quiz on Slido**: [Slido Link](https://app.sli.do/event/px7Ds71gNCMa1BeTcAatGa)