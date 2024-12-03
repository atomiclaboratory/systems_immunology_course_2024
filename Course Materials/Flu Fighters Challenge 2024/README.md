# **Flu Fighters: The Ultimate Immunogenicity Challenge 🤖🧬💉**

![Flu Fighters Logo](https://github.com/atomiclaboratory/systems_immunology_course_2024/blob/main/Course%20Materials/Flu%20Fighters%20Challenge%202024/images/logo_full.png)

Welcome to **Flu Fighters: The Ultimate Immunogenicity Challenge**, where your mission is to predict vaccine responsiveness to the **Live Attenuated Influenza Vaccine (LAIV)** and uncover the secrets of vaccine immunogenicity. This is not your average data science task—this is the **most difficult challenge yet**! Why? Let’s break it down.

---

## 🌟 Why this challenge is unique:

1. **Immune Complexity**: Vaccine-induced immunity involves interactions between multiple immune compartments—humoral, cellular, and mucosal—all influenced by baseline immune states.  
2. **Interindividual Variability**: No two individuals respond to a vaccine in exactly the same way, and biological outliers make predictions even harder.  
3. **High-Dimensional Data**: You’ll work with transcriptomics, cellular data, and serological markers, all integrated into a single dataset.  
4. **Missing Data and Noise**: Real-world datasets like this one come with challenges like missing values and measurement noise.  

Are you ready to tackle one of the most critical and complex questions in immunology and data science? Let's find out which team will become the **next best Flu Fighters on the planet**! 🌍💪

---

## 📋 **Challenge Overview**

The dataset contains data from **244 children** (aged 2–5 years) vaccinated with LAIV. Your task is to predict **vaccine responsiveness** (immunogenicity) based on **baseline immune features**. Responsiveness reflects how well a vaccine elicits an immune response, spanning humoral, cellular, and mucosal immunity.

For more details, refer to the publication that describes this cohort:  
**[Effect of a Russian-backbone live-attenuated influenza vaccine on shedding and immunogenicity among children in The Gambia](https://github.com/atomiclaboratory/systems_immunology_course_2024/blob/main/Course%20Materials/FLU%20PREDICTION%20CHALLENGE/reading%20materials/2019%20Lindsey%20LAIV%20phase%204%20study.pdf)**  
(*Lindsey, Benjamin B et al., The Lancet Respiratory Medicine, 2019.*)

📌 **Figure 1. Study Design Overview.**  
![Study Design Overview](https://github.com/atomiclaboratory/systems_immunology_course_2024/blob/main/Course%20Materials/Flu%20Fighters%20Challenge%202024/images/study%20design.png)

---

### ‼️ Why It Matters:
- **Understanding Immunogenicity**: Key to improving vaccine design and targeting specific populations.  
- **Guiding Personalized Strategies**: Accurate predictions can inform tailored vaccination approaches.  
- **Unique LAIV Features**: This intranasal vaccine stimulates robust mucosal IgA immunity, moderate T-cell responses, and generally low systemic HAI antibody titers.

This challenge mimics **real-world vaccine research**, where interindividual variability and biological noise create significant hurdles.

---

## **How Vaccine Responsiveness Is Defined**

### 📈 **Definition**
Vaccine responsiveness is measured as the **fold-change** in immune responses, calculated as:  

Fold-Change = Response on Day 21 Post-Vaccination / Baseline Response (Day 0)

This approach ensures that **pre-existing immune states** are accounted for when assessing vaccine-induced changes. By using the fold-change, we can compare individuals who start at very different baseline levels.

### ‼️ **Why This Matters**
Using fold-change helps avoid misinterpreting absolute response values. For example:
- A participant with **high baseline levels** of antibodies may exhibit a smaller increase post-vaccination compared to a participant with **low baseline levels**, even though their final antibody levels remain higher.
- Conversely, a participant with **low baseline levels** may show a dramatic fold-change increase post-vaccination, reflecting a strong vaccine response despite lower absolute levels.

### **Example**
| Participant | Baseline Response (Day 0) | Post-Vaccine Response (Day 21) | Fold-Change | Interpretation |
|-------------|----------------------------|---------------------------------|-------------|----------------|
| A           | 200                        | 400                             | 2.0         | Moderate response, given the high baseline. |
| B           | 20                         | 60                              | 3.0         | Strong response, despite starting low. |
| C           | 200                        | 220                             | 1.1         | Poor response, even with high starting levels. |

In this example:
- Participant **B** demonstrates a stronger responsiveness to the vaccine compared to **A**, even though **A** has higher absolute values post-vaccination.  
- Participant **C** shows minimal vaccine-induced changes, indicating poor responsiveness.  

This strategy captures the **individualized nature** of immune responses, ensuring fair comparisons across diverse pre-existing immune states.

---

### 📅 **Timeline and Guidelines**

- **Nov 26th**: **Self-paced**  
  - Teams will work independently to develop a **strategy** for predictive modeling.  

- **Dec 3rd**: **Team-work in the class** with the instructor.  
  - Showcase your strategy to the instructor and discuss any final questions or ideas to **improve your approach**.  

- **Dec 4th**: **Submission Deadline**  
  - Submit your final models and analysis by **end of the day**. Each team should email their final model to Dr. Tomic.

- **Dec 5th**: **Team Presentations**  
  - Each team will present their **strategy for machine learning predictive modeling**.  
  - A winner will be announced based on creativity, execution, and predictive performance.  

---

## 📊 **Dataset Description**

The dataset contains **predictor variables** (baseline immune data, demographics, and transcriptomics) and **outcome variables** (vaccine responsiveness).

### **📥 Predictors**
📌 **Figure 2. Overview of the baseline measurements included in the dataset.** 
![baseline predictive modeling](https://github.com/atomiclaboratory/systems_immunology_course_2024/blob/main/Course%20Materials/Flu%20Fighters%20Challenge%202024/images/baseline%20predictive%20modeling%20overview.png)

#### 🧑‍🔬 **Demographics**
- `subid1`: Unique participant ID.  
- `sex` (🔵/🔴): Biological sex (`M` or `F`).  
- `age_months`: Age of the participant in months.  
- `z_score_continuous`: Weight-for-height Z-score (nutritional status).  
- `year`: Year of sample collection (2017 or 2018).  

#### 🧬 **Baseline Immune Features**
- **Blood Transcriptomics**: Pathway activity captured by **Gene Ontology (GO)** terms, e.g., `blood_baseline_go.0006415` (translation).  
- **Nasal Transcriptomics**: Pathway activity in nasal samples, e.g., `nasal_baseline_go.0006968` (defense response to virus).  
- **Immune Cell Subsets**:
  - `v0_mdcs`: Myeloid dendritic cells (mDCs).  
  - `v0_pdcs`: Plasmacytoid dendritic cells (pDCs).  
  - `v0_classical_monocytes`, `v0_intermediate_monocytes`, `v0_nonclassical_monocytes`: Monocyte subsets.  
- **Viral and Bacterial Load**:
  - `v0_resp_virus_positive`: Presence of 14 different respiratory viruses (flu, adenoviruses, rhinoviruses, coronaviruses, etc.) detected via RT-PCR at baseline.  
  - `v0_pneumo_ng_log10copies_ul`: Nasal *Streptococcus pneumoniae* density (log10 copies per µL).  

---

### **🎯 Outcome Variables**

#### 🔬 **Vaccine Responsiveness**
These variables measure vaccine-induced immune responses across humoral, cellular, and mucosal immunity:

##### **Humoral Responses**
- `h1_hai_gmt_fold_change`: Responsiveness in HAI titers for H1N1 (serum antibody response blocking virus-host interaction).  
- `h3_hai_gmt_fold_change`: Responsiveness in HAI titers for H3N2.  
- `ph1n1_ha_iga_fold_change`: Responsiveness in mucosal IgA binding to H1N1 hemagglutinin.  

##### **Cellular Responses**
- `h1_cd4_ifng_fold_change`: Responsiveness in CD4+ IFN-γ T cell responses for H1N1 (cellular immunity indicator).  
- `h3_cd8_il2_fold_change`: Responsiveness in CD8+ IL-2 T cell responses for H3N2.  

##### **IVPM Antibody Binding**
- `nc99_ivpm_h1_fold_change`: Responsiveness in antibody binding to HA from A/New Caledonia/20/1999, measured using a high-throughput HA microarray platform which allows to test presence of antibodies that can bind vaccine-formulated influenza starins and historical and drifted inlfuenza strains not included in the vaccine forumation.

---

### **📂 Dataset Files**

**`flu_fighters.csv`**: The entire dataset with 244 participants, including predictors and outcome variables.

---

## 🧠 **Evaluation Metrics**

Submissions will be evaluated using:
- **AUC (Area Under the Curve)** on the test set.  
- **Biological Interpretation**: Importance of variables and insights into the model’s findings.

---

## 🏆 **Awards**

1. 🥇 **1st Place**:  
   - Certificate of **Awesomeness**.  
   - Special **Giant Microbe Trophy** for the team.  

2. 🥈 **2nd Place**:  
   - Certificate of **Excellence**.  
   - Giant Microbes for each team member.  

3. 🥉 **3rd Place**:  
   - Certificate of **Achievement**.  
   - Giant Microbes for each team member. 

---

## 🚀 **Get Started**

This section provides ideas and suggestions to help you and your team tackle the Flu Fighters challenge. These are not strict guidelines but are meant to inspire your process and help you think critically about the task. Feel free to be creative and come up with your unique approach! 🌟

---

### 🎯 **Step 1: What Are You Predicting?**

Before diving into the dataset, decide on your **research question**:  
1. Are you predicting a specific **outcome**, such as:
   - 🧪 **Humoral Responses**: E.g., `h1_hai_gmt_fold_change` (HAI titers for H1N1).  
   - 🧬 **Cellular Responses**: E.g., `h1_cd4_ifng_fold_change` (T-cell cytokine production).  
   - 🧫 **IVPM Antibody Binding**: E.g., `nc99_ivpm_h1_fold_change` (binding to flu antigens).  
2. Are you exploring **clusters of individuals** based on shared vaccine responsiveness patterns?  
   - Example groups:  
     - Group A: High IgA responses, low T-cell responses.  
     - Group B: Strong T-cell activation, moderate humoral immunity.  

💡 **Idea**: For a specific outcomes, such as HAI responders, set up threshold HAI >4 as high responders and all below as low responders.
For clustering, try different algorithms and compare results:  
  - Use PANDORA’s automated clustering options if available.  
  - Evaluate cluster quality with metrics like silhouette scores or biological interpretability. 
 

---

### 🧠 **Step 2: Which Measurements Will You Use?**

**Questions to Address:**
1. Which predictors (features) will you use to build your model?  
2. Will you include only **baseline (Day 0)** data, or also early post-vaccination data (Days 2, 7)?  
3. Do you need **Day 21 (V21)** data?  

**Features to Consider:**
- **Demographics**:  
  - Age (`age_months`), sex (`sex`), and nutritional status (`z_score_continuous`).  
  - Example: Does age correlate with stronger T-cell responses?  

- **Baseline Immune Data**:  
  - 🧬 **Blood Transcriptomics**: Gene Ontology terms like `blood_baseline_go.0006415` (translation).  
  - 🦠 **Nasal Transcriptomics**: Pathway activity in nasal samples, e.g., `nasal_baseline_go.0006968` (defense response to virus).  
  - 🧪 **Immune Cell Subsets**: Baseline mDCs (`v0_mdcs`), pDCs (`v0_pdcs`), and monocyte subsets.  

- **Post-Vaccination Data**:
  - 🧪 **Day 2 and Day 7**: Intermediate immune activation (e.g., `v2_mdcs`, `v7_pdcs`).  
  - 🧬 **Fold-change transcriptomics**: Transcriptomic changes from Day 0 to Day 21.

💡 **Idea**: Use Day 2 and Day 7 data to explore how early immune responses influence final vaccine outcomes. For example:
  - Are individuals with higher **Day 2 monocyte activation** better systemic antibody responders by Day 21?  

---

### ⚙️ **Step 3: How Will You Model It?**

**Questions to Address:**
1. How will you preprocess your data?  
   - Will you handle missing values with imputation or use **Mulset** for noise reduction?  
   - Will you remove highly correlated features ( or drop near-zero variance features?  
2. How will you partition your data into training and test sets?  
3. What algorithms will you use?

Here are some steps and ideas to help structure your modeling process:  

#### **1. Data Preprocessing**  
- 🧹 **Clean the data**: Handle missing values with imputation (median/mean) or try the **Mulset algorithm** to reduce noise.  
- 🔗 **Feature selection**: Will you remove highly correlated features (Pearson correlation > 0.85) or drop near-zero variance (NZV) features if they add noise.  
- 🧮 **Normalization**: Do you need to scale your predictors?

💡 **Idea**: Mulset generates multiple datasets which increases the predictive modeling time - do you need to select all datasets generated by mulset?

---

#### **2. Splitting the Data**  
- 📊 Partition the dataset into **training** and **test sets**:  
  - What determines how will you split your dataset for training and testing?

---

#### **3. Choosing Algorithms**  
- 🛠️ Start simple:  
  - Linear regression for continuous outcomes.  
  - Decision trees or random forests for classification.  
- 🚀 Explore advanced options:  
  - Gradient boosting (e.g., XGBoost, CatBoost).  
  - Neural networks for complex relationships.  
- 🤖 Use automated tools like **SIMON** to test multiple AI algorithms.

💡 **Idea**: Automated ML approach in SIMON can increase performance, but computationally intensive - start with the analysis early!

---

### 🔍 **Step 4: How Will You Evaluate Your Model?**

**Questions to Address:**
1. How will you measure model performance?  
2. How will you ensure your model is not overfitting?  
3. What biological insights can you draw from your model?

**Suggestions:**
- **Evaluation Metrics**:
  - 📈 Use AUC (Area Under the Curve) for classification.  
  - 🎯 Use precision, recall, F1-score for imbalanced data.  
  - 🏆 Assess sensitivity/specificity for true positives and negatives.  

- **Overfitting**:
  - Compare training and test performance to ensure generalizability.  

- **Biological Insights**:
  - 🧬 Look at feature importance scores—are the predictors biologically meaningful?  
  - 🔬 Interpret the model outputs to relate them to known immune mechanisms or discover new patterns.

💡 **Idea**: Use visualization tools like variable improtance score table, hierarchical clustering or t-SNE to explain your results.

---

### 🎨 **Step 5: Presenting Your Work**

When presenting on **Dec 5th**, make sure to cover:  
1. **Research Question**: What did you aim to predict or explore?  
2. **Methods**: What modeling strategy did you use, and why?  
3. **Results**: Show performance metrics and highlight interesting findings.  
4. **Biological Meaning**: What insights did your model uncover about LAIV vaccine responses?

---

## 💡 **Hints and Tips**

Here are some helpful hints based on **Module 4 content**:

1. **SIMON**: Use this automated ML platform to improve modeling and streamline the prediction process.  
2. **Mulset Algorithm**: This algorithm reduces noise and handles missing data effectively by creating smaller datasets.  
3. **PANDORA's t-SNE Function**: Utilize automated t-SNE for high-dimensionality reduction and improved clustering.  
4. **Clustering Algorithms**: Experiment with different clustering approaches to identify responder profiles.  
5. **Feature Selection**: Not all features are equally useful. Focus on those with the highest predictive power.

---

## 🌟 **Good Luck!**

Remember, there’s no single right way to approach this challenge. Be creative, think critically, and have fun exploring the data!