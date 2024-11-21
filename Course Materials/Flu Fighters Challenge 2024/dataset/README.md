# Legend or Key for Variables in the FluFighters Dataset 🦠💉📊

---

## 1. Blood Gene Expression (Baseline and Fold Change) 🩸🧪

**Variables:**
- `blood_baseline_go.*`
- `blood_foldchange_go.*`

**Description:**
- These variables represent the expression levels of genes associated with specific Gene Ontology (GO) terms in blood samples.
- **Baseline Measurements (`blood_baseline_go.*`):** Indicate the initial gene expression levels before vaccination.
- **Fold Change Measurements (`blood_foldchange_go.*`):** Represent the change in gene expression levels 2 days after vaccination relative to baseline.
- **Gene Ontology (GO):** A standardized system that classifies genes based on their biological processes, cellular components, and molecular functions.

---

## 2. Nasal Gene Expression (Baseline and Fold Change) 👃🧪

**Variables:**
- `nasal_baseline_go.*`
- `nasal_foldchange_go.*`

**Description:**
- Similar to the blood gene expression variables, these represent gene expression levels in nasal samples.
- **Importance:** Nasal mucosa is a primary site for respiratory infections like influenza, making nasal gene expression critical for understanding mucosal immunity.

---

## 3. Hemagglutination Inhibition (HAI) Responses 🦠💉

**Variables:**
- `h1_hai_v0_gmt`, `h1_hai_v21_gmt`, `h3_hai_v0_gmt`, `h3_hai_v21_gmt`, `b_hai_v0_gmt`, `b_hai_v21_gmt`
- `h1_hai_gmt_fold_change`, `h3_hai_gmt_fold_change`, `b_hai_gmt_fold_change`
- `max_hai_responder`

**Description:**
- **HAI Assay:** Measures the ability of antibodies in the serum to prevent the agglutination of red blood cells by the influenza virus, indicating neutralizing antibody levels.
- **Viruses:**
  - `h1_`: HAI against H1N1
  - `h3_`: HAI against H3N2
  - `b_`: HAI against Influenza B
- **Timepoints:**
  - `_v0_gmt`: Geometric Mean Titer (across all three vaccine influenza strains) at baseline (pre-vaccination).
  - `_v21_gmt`: Geometric Mean Titer (across all three vaccine influenza strains) 21 days post-vaccination.
- **Interpretation:**
  - **Seroconversion:** An increase in HAI titer of more than 4-fold post-vaccination is considered seroconversion, and is associated with the 50% reduction in influenza disease severity.
  - **Seropositivity:** An HAI titer above 40 is considered seropositive, suggesting protective immunity.
- **Assay Procedure:**
  - Patient serum is mixed with standardized virus amounts.
  - Red blood cells are added; if antibodies are present, they inhibit hemagglutination.

---

## 4. Immunoglobulin A (IgA) Responses 🧫🛡️

**Variables:**
- `ph1n1_ha_iga_v0`, `ph1n1_ha_iga_v21`, `h3n2_ha_iga_v0`, `h3n2_ha_iga_v21`, `bvic_ha_iga_v0`, `bvic_ha_iga_v21`
- `ph1n1_na_iga_v0`, `ph1n1_na_iga_v21`, `h3n2_na_iga_v0`, `h3n2_na_iga_v21`, `bvic_na_iga_v0`, `bvic_na_iga_v21`
- `ph1n1_ha_iga_fold_change`, `h3n2_ha_iga_fold_change`, `bvic_ha_iga_fold_change`
- `max_iga_responder`

**Description:**
- **IgA Antibodies:** Play a crucial role in mucosal immunity by neutralizing pathogens at entry points.
- **Measurements:**
  - Levels of IgA specific to hemagglutinin (HA) and neuraminidase (NA) antigens of influenza viruses.
- **Timepoints:**
  - `_v0`: Baseline levels.
  - `_v21`: Levels 21 days post-vaccination.
- **Fold Change:** Indicates the increase in IgA levels post-vaccination.

---

## 5. T Cell Responses (CD4⁺ and CD8⁺ Cells) 🦠🔬

**Variables:**
- `h1_v0_cd4_ifng`, `h1_v21_cd4_ifng`, `h1_v0_cd4_il2`, `h1_v21_cd4_il2`
- Similar variables for `cd8` cells and other influenza strains (`h3`, `hmnp`, `hab`, `bmnp`)
- Fold change variables like `h1_cd4_ifng_fold_change`
- `max_mnp_cd4_responder`, `max_mnp_cd8_responder`

**Description:**
- **Function:** Measure cytokine production by T cells in response to influenza antigens.
- **Cytokines:**
  - **IFN-γ (Interferon gamma):** Indicates Th1 response, important for antiviral immunity.
  - **IL-2 (Interleukin-2):** Supports T cell proliferation.
- **Cell Types:**
  - **CD4⁺ T Cells:** Helper cells that orchestrate immune responses.
  - **CD8⁺ T Cells:** Cytotoxic cells that kill infected cells.
- **Assay Procedure:**
  - Cells are stimulated with antigens and cytokine production is measured via flow cytometry or ELISPOT.

---

## 6. Influenza Virus Protein Microarray (IVPM) Responses 🦠🧬

**Variables:**
- `nc99_ivpm_h1_v0`, `nc99_ivpm_h1_v21`, `mich15_h1_ivpm_v0`, etc.
- Fold change variables like `nc99_ivpm_h1_fold_change`

**Description:**
- **IVPM Assay:** Detects antibody responses to multiple influenza strains simultaneously using microarray technology.
- **Purpose:** Evaluates the breadth of the immune response.

---

## 7. Antibody-Dependent Cellular Cytotoxicity (ADCC) and Secretory IgA (SIgA) Responses 🛡️🔬

**Variables:**
- `ch6_adcc_auc_v0`, `ch6_adcc_auc_v21`, `ch6_adcc_auc_fold_change`
- `ch6_siga_v0`, `ch6_siga_v21`, `ch6_siga_fold_change`
- Similar variables for `ch7`

**Description:**
- **ADCC:**
  - **Function:** Assesses the ability of antibodies to recruit natural killer (NK) cells to destroy infected cells.
  - **Measurement:** Area Under the Curve (AUC) represents the overall ADCC activity.
- **SIgA:**
  - **Function:** Secretory IgA antibodies protect mucosal surfaces by neutralizing pathogens.

---

## 8. Neuraminidase binding assay titers 🧪🧬

**Variables:**
- `n1_titer_v0`, `n1_titer_v21`, `n2_titer_v0`, `n2_titer_v21`
- `n1_titer_fold_change`, `n2_titer_fold_change`

**Description:**
- **NI Assay:** Measures antibodies that bind neuraminidase (NA) from group 1 (H1N1) and group 2 (H3N2) flu viruses.
- **Importance:** NA antibodies have cross-reactivity.

---

## 9. Viral Shedding 🌬️🦠

**Variables:**
- `h1_v2_shed`, `h3_v2_shed`, `b_v2_shed`
- `h1_v7_shed`, `h3_v7_shed`, `b_v7_shed`

**Description:**
- **Definition:** Detection of virus in nasal swabs post-vaccination.
- **Timepoints:**
  - `_v2_shed`: Viral shedding at day 2.
  - `_v7_shed`: Viral shedding at day 7.
- **Significance:** Indicates active viral replication and potential transmissibility.

---

## 10. Demographics and Baseline Characteristics 👤📋

**Variables:**
- `year`, `sex`, `age_months`, `z_score_continuous`

**Description:**
- **Year:** Study year or participant's birth year.
- **Sex:** Male or Female.
- **Age in Months:** Participant's age at the time of study.
- **Z-Score:** Standardized score indicating nutritional status or growth parameters.

---

## 11. Seropositivity and Seroconversion Status 🛡️🧪

**Variables:**
- `h1_v0_seropositive`, `h3_v0_seropositive`, `b_v0_seropositive`

**Description:**
- **Seropositivity:** Indicates the presence of protective antibody levels at baseline.
- **Criteria:** HAI titer above 40 is considered seropositive.
- **Implication:** Participants already have some immunity prior to vaccination.

---

## 12. Monocyte and Dendritic Cell Counts 🧪🔬

**Variables:**
- **Myeloid Dendritic Cells (mDCs):**
  - `v0_mdcs`, `v2_mdcs`, `v7_mdcs`
- **Plasmacytoid Dendritic Cells (pDCs):**
  - `v0_pdcs`, `v2_pdcs`, `v7_pdcs`
- **Monocytes:**
  - `v0_classical_monocytes`, `v2_classical_monocytes`, `v7_classical_monocytes`
  - `v0_intermediate_monocytes`, etc.

**Description:**
- **Function:** Dendritic cells and monocytes are crucial for antigen presentation and initiating immune responses.
- **Timepoints:** Counts at baseline and post-vaccination days 2 and 7.

---

## 13. T Follicular Helper (Tfh) Cells 🦠🔬

**Variables:**
- `tfh_cxcr3_icos_pd1_v0`, `tfh_cxcr3_icos_pd1_v7`

**Description:**
- **Role:** Tfh cells assist B cells in producing high-affinity antibodies.
- **Markers:**
  - **CXCR3, ICOS, PD-1:** Surface proteins used to identify activated Tfh cells.
- **Significance:** Increased Tfh cells correlate with better antibody responses.

---

## 14. Baseline Respiratory Virus and Pneumococcus Detection 🦠🩺

**Variables:**
- `v0_resp_virus_positive`
- `v0_pneumo_ng_log10copies_ul`

**Description:**
- **Respiratory Virus Positive:** Indicates the presence of 14 respiratory viruses at baseline, which could affect immune responses.
- **Pneumococcus Load:** Quantifies nasal carriage of *Streptococcus pneumoniae*.

---

## 15. Fold Change in Immune Responses 📈🧪

**Variables:**
- Variables ending with `_fold_change` for various assays (e.g., `h1_cd4_ifng_fold_change`)

**Description:**
- **Calculation:** Post-vaccination value divided by baseline value.
- **Purpose:** Assesses the magnitude of the immune response induced by vaccination.

---

## 16. Max Responder Variables 🏅📊

**Variables:**
- `max_hai_responder`, `max_iga_responder`, `max_mnp_cd4_responder`, `max_mnp_cd8_responder`

**Description:**
- **Definition:** Identifies participants with the highest response in each category.
- **Criteria:** Based on predefined thresholds for significant immune responses (4-fold increase for HAI, and 2-fold increase for others).