# 🎃 Bayesian and Discriminant Analysis 📉🧬

## Team 6 - Dennis Noble 🧛‍💀🕸️

**Members:**
- Amanda Adams 🧙‍♀️
- Grace Tugado 🧛‍♀️
- Elizabeth Esquivel 👻
- Jack Rodrigue 🧟‍♂️
- Wai Yuen (Wylliam) Zheng ☠️

This team will introduce Bayesian and discriminant analysis, comparing Naive Bayes (NB) and Linear Discriminant Analysis (LDA), highlighting their strengths, weaknesses, and key differences.

---

## 🎃 Activities 👻

1. **30-Minute Presentation by Team Noble and Group Discussion (Until 4:00 PM)** 🎤☠️  
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

This data is derived from the study ["Divergent trajectories of antiviral memory after SARS-CoV-2 infection"](https://github.com/atomiclaboratory/systems_immunology_course_2024/blob/main/Course%20Materials/MODULE%204%20-%20Weeks%207-14/reading%20materials/2022%20PITCH%20study.pdf) published in *Nature Communications* (2022). The dataset provided to students is a simplified version with only day 28 post-infection measurements, focusing on predicting long-term immunity responses.

---

## 🎃 Analysis Parameters 🕸️

- **Outcome**: N_IgG_responder
- **Predictors**: All measurements except sex
- **Training Set**: 75% of the data
- **Test Set**: 25% of the data

### Preprocessing 🧛‍♀️

- **Centering and Scaling**:  
  **Centering** subtracts the mean from each feature, and **scaling** divides by the standard deviation, standardizing the data so all features contribute equally to model training.

  **Example Calculation**:
  
  - Original Data: [15, 25, 35]
  - Mean: (15 + 25 + 35) / 3 = 25
  - Standard Deviation (SD): √[((15-25)² + (25-25)² + (35-25)²) / 3] = 8.16

  | Original Value | Centered (Value - Mean) | Scaled (Centered / SD) |
  |----------------|-------------------------|-------------------------|
  | 15            | 15 - 25 = -10           | -10 / 8.16 ≈ -1.22     |
  | 25            | 25 - 25 = 0             | 0 / 8.16 = 0           |
  | 35            | 35 - 25 = 10            | 10 / 8.16 ≈ 1.22       |

- **Median Imputation**:  
  Replaces missing values with the median of the column, which is less affected by outliers compared to the mean.

  **Example Calculation**:

  - Original Data (with NaN): [10, NaN, 30, 20]
  - Median: Sort [10, 20, 30] → Median is 20

  | Original Data | Imputed Data (replace NaN with median) |
  |---------------|----------------------------------------|
  | 10           | 10                                     |
  | NaN          | 20                                     |
  | 30           | 30                                     |
  | 20           | 20                                     |

- **Correlation and Zero/Near Zero Variance Filtering**:  
  Removes features with high correlation (redundant information) and those with near-zero variance (little variability).

  **Example Calculation**:

  - **Correlation**: Feature 1 and Feature 2 have a high correlation. Correlation calculation:
    - Feature 1: [1, 2, 3]
    - Feature 2: [1.01, 2.05, 3.02]
    - Correlation coefficient ≈ 0.99 (highly correlated)

  - **Variance of Feature 3** (near-zero variance):
    - Feature 3 values: [0.1, 0.1, 0.1]
    - Variance = 0 (no variability)

  | Feature 1 | Feature 2 (highly correlated with Feature 1) | Feature 3 (near-zero variance) |
  |-----------|---------------------------------------------|---------------------------------|
  | 1         | 1.01                                        | 0.1                             |
  | 2         | 2.05                                        | 0.1                             |
  | 3         | 3.02                                        | 0.1                             |

  Since Feature 2 is highly correlated with Feature 1, and Feature 3 has near-zero variance, both would be removed in preprocessing.

---

## Team-tasks 🧟‍♂️🧟‍♀️🧟‍♂️🧟‍♀️
1. **Comparison of NB and LDA**: Which algorithm performs better based on AUC?

2. **Feature Importance**: Which features predict being a high responder at 6 months?

3. **Algorithm Comparison**: Run all 42 Bayesian and discriminant analysis algorithms. Which one performs best?


---

## 🕸️ References 🕸️

- **Paper**: ["Divergent trajectories of antiviral memory after SARS-CoV-2 infection"](https://github.com/atomiclaboratory/systems_immunology_course_2024/blob/main/Course%20Materials/MODULE%204%20-%20Weeks%207-14/reading%20materials/2022%20PITCH%20study.pdf), March 10, 2022, Article number: 1251
- **Authors**: Adriana Tomic, Donal T. Skelly, Ane Ogbe, et al.

---
🎃👻 Happy Halloween! 🎃👻
