# Decision Trees and Ensemble Methods 🌳🔀
**Team 5 - Polly Matzinger**

### Members:
- Selena Halabi
- Kewei Ye
- Jordan Smiley
- Lexi Wittstadt (and their pets 😉)

This team will introduce decision tree and ensemble methods, focusing on the algorithms **C5.0** and **Random Forest (RF)**. They will highlight each algorithm's strengths, weaknesses, and key differences, especially in the context of predicting immunological responses.

---

## Activities 📚

1. **Presentation by Team Matzinger and Group Discussion (Until 4:00 PM) 🎤**
   - Team Matzinger will introduce decision tree algorithms and ensemble methods, emphasizing C5.0 and Random Forest.

2. **Hands-on Predictive Modeling using PANDORA (4:00 PM - 5:15 PM) 💻📊**
   - In this session, you will apply decision tree and ensemble methods to predict immune response outcomes using the COVID-19 dataset.
   - **Goal**: Predict which individuals are likely to have high antibody levels six months after infection based on their immunological measurements taken 28 days post-infection.

---

## 📊 Dataset Overview

The dataset includes the following variables:

- **Sex**: Biological sex of the participant
- **PseudoNA_Abs, ADCD, ADMP, ADNKA, ADNP**: Pseudo-neutralizing antibodies and antibody immune cell functions
- **S_IgA, S_IgG1, S_IgG2, S_IgG3, S_IgG4, S_IgM, S_IgA_memB_SARS_CoV2**: Various spike-specific antibodies
- **MemB_229E, MemB_HKU1, MemB_NL63, MemB_OC43**: Memory B cell responses for different seasonal coronaviruses
- **SARS-CoV-2 Measures**: Includes variables like SARS-CoV-2 N_MSD, RBD_MSD, and S_MSD
- **Proliferation markers**: Proliferation rates for various immune cell types
- **ELISpot markers**: T cell responses measured by ELISpot
- **Outcome Variable**: **N_IgG_responder** – Indicates if the individual is a high responder (high anti-N SARS-CoV-2 antibodies 6 months post-infection)

This data is derived from the study *Divergent trajectories of antiviral memory after SARS-CoV-2 infection* (Nature Communications, 2022). We are using day 28 post-infection measurements to predict long-term immunity responses.

---

## ML Analysis Parameters

- **Outcome**: **N_IgG_responder**
   - The target variable predicting if an individual will have high antibody levels 6 months post-infection.
   
- **Predictors**: All measurements except sex
   - These immunological measurements serve as the predictors in the model.

- **Training Set**: 75% of the data (n=56)
   - Used to train the model and help it learn patterns.

- **Test Set**: 25% of the data (n=18)
   - Used to assess the model’s performance on unseen data.

---

## Preprocessing

1. **Centering and Scaling**:
   - Standardizes data so all features contribute equally to the model training.

2. **Median Imputation**:
   - Replaces missing values with the column median, which is less influenced by outliers.

3. **Correlation and Zero/Near Zero Variance Filtering**:
   - Removes features with high correlation and low variance.

---

## Team Tasks

- **Comparison of RF and C5.0**: Which algorithm can predict the best immune responders?
- **Algorithm Comparison**: Compare both RF and C5.0 to NB and LDA algorithms we used in the last class? Which is better?
- **Feature Importance**: Identify key predictors of a high antibody response at 6 months.

---

## Self-Paced Analysis Tasks ⏳

As tree and ensemble methods can be computationally intensive, you can perform the following tasks at your own pace:

1. **Run All 35 Ensemble Methods**:
   - Test all available ensemble methods in PANDORA and compare their performance to see which algorithm works best for predicting high responders.
   
2. **Run All 24 Tree Methods Separately**:
   - Explore all available tree-based methods individually to determine which one yields the most accurate predictions for the given dataset.

These additional analyses will help you understand the variability in performance across different algorithms.


