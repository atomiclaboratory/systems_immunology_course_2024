# 🎃 Bayesian and Discriminant Analysis 📉🧬

## Team 6 - Dennis Noble 🧛‍💀🕸️

**Members:**
- Amanda Adams 🧙‍♀️
- Grace Tugado 🧛‍♀️
- Elizabeth Esquivel 👻
- Jack Rodrigue 🧟‍♂️
- Wai Yuen (Wylliam) Zheng 🧛‍♂️

This team will introduce Bayesian and discriminant analysis, comparing Naive Bayes (NB) and Linear Discriminant Analysis (LDA), highlighting their strengths, weaknesses, and key differences.

---

## 🎃 Activities 👻

1. **30-Minute Presentation by Team Noble and Group Discussion (Until 4:00 PM)** 🎤🕸️  
   Team Nobel will present their comparison of Bayesian and discriminant analysis.

2. **Hands-on Predictive Modeling using PANDORA (4:00 PM - 5:15 PM) 💻📊** 🎃  
   Using the dataset from the PITCH study, students will predict N_IgG_responders (individuals with particularly high SARS-CoV-2 antibodies recognizing N protein 6 months post-infection) using Naive Bayes and LDA, along with other Bayesian and discriminant analysis algorithms. The efficiency of each algorithm will be compared.

---

## 📊 Dataset Overview 🎃

The dataset includes measurements from the following variables:
- **Sex**: Biological sex of the participant
- **PseudoNA_Abs, ADCD, ADMP, ADNKA, ADNP**: Pseudo-neutralizing antibodies and Ab immune cell functions
- **S_IgA, S_IgG1, S_IgG2, S_IgG3, S_IgG4, S_IgM, S_IgA_memB_SARS_CoV2**: Various spike-specific Abs
- **MemB_229E, MemB_HKU1, MemB_NL63, MemB_OC43**: Memory B cell responses for different seasonal coronaviruses
- **SARS-CoV-2 Measures**: Includes variables like SARS-CoV-2 N_MSD, RBD_MSD, and S_MSD
- **Proliferation markers**: Proliferation rates for various immune cell types
- **ELISpot markers**: T cell responses measured by ELISpot
- **Outcome Variable**: **N_IgG_responder** – Indicates if the individual is a high responder (high anti-N SARS-CoV-2 antibodies 6 months post-infection)

This data is derived from the study "Divergent trajectories of antiviral memory after SARS-CoV-2 infection" published in *Nature Communications* (2022).
The dataset provided to students is a simplified version with only day 28 post-infection measurements, focusing on predicting long-term immunity responses.

---

## 🎃 Analysis Parameters 🕸️

- **Outcome**: N_IgG_responder
- **Predictors**: All measurements except sex
- **Training Set**: 75% of the data
- **Test Set**: 25% of the data

### Preprocessing 🧛‍♀️
- **Centering** and **Scaling** of data for consistency.
- **Median Imputation** to handle missing values.
- **Correlation** and **Zero/Near Zero Variance Filtering** to remove redundant or non-informative predictors.

### Analytical Questions 🎃
1. **Comparison of NB and LDA**: Which algorithm performs better based on AUC?
2. **Feature Importance**: Which features predict being a high responder at 6 months?
3. **Algorithm Comparison**: Run all 42 Bayesian and discriminant analysis algorithms. Which one performs best?
4. **Model Generalizability**: How can the generalizability of these models be confirmed?

---

## 🕸️ References 🕸️

- **Paper**: *Divergent trajectories of antiviral memory after SARS-CoV-2 infection*  
  *Nature Communications*, March 10, 2022, Article number: 1251
- **Authors**: Adriana Tomic, Donal T. Skelly, Ane Ogbe, et al.

---
🎃👻 Happy Halloween! 🎃👻
