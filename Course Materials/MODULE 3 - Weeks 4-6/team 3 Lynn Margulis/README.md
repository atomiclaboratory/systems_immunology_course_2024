# ⚧💉 Immune System Adaptation During Gender-Affirming Testosterone Treatment

## Team 3 - Lynn Margulis

**Members:**
- Kaavya Akula  
- Joseph Soto  
- Marek Pinto  
- Julia Nowak

This team will investigate how gender-affirming testosterone treatment affects the immune system, focusing on changes in immune cell populations and inflammatory markers. They will explore the broader implications of hormone therapy on immune function and gender-specific immune adaptations.

---

## Presentation Overview

**Topic:** *Immune system adaptation during gender-affirming testosterone treatment*  
**Paper Reference:**  
- Tadepally Lakshmikanth, Camila Consiglio, Fabian Sardh, Rikard Forlin, Jun Wang, Ziyang Tan, Hugo Barcenilla, Lucie Rodriguez, Jamie Sugrue, Peri Noori, Margarita Ivanchenko, Laura Piñero Páez, Laura Gonzalez, Constantin Habimana Mugabo, Anette Johnsson, Henrik Ryberg, Åsa Hallgren, Christian Pou, Yang Chen, Jaromír Mikeš, Anna James, Per Dahlqvist, Jeanette Wahlberg, Anders Hagelin, and Petter Brodin  
- *Nature*, volume 633, pages 155–164 (2024)  
- [Link to Paper](https://www.nature.com/articles/s41586-024-07789-z)  

### Abstract Summary 📄

In this study, the authors conducted a longitudinal analysis of 23 transgender men undergoing gender-affirming testosterone treatment to investigate the immune system adaptations during therapy. The results showed that testosterone modulates a cross-regulated axis between type-I interferon and tumor necrosis factor (TNF). Specifically, testosterone attenuates type-I interferon responses in plasmacytoid dendritic cells and monocytes while potentiating monocyte-mediated TNF, interleukin-6, and interleukin-15 production. These findings provide insights into how testosterone therapy impacts immune function, with broader implications for sex-divergent immune responses in both transgender and cisgender individuals.

---

## Activities 📚

1. **30-Minute Presentation by Team Margulis (Until 4:00 PM)**  
   Team Margulis will present their analysis on how gender-affirming testosterone treatment affects the immune system, with a specific focus on changes in immune cell populations and inflammatory markers.

2. **30-Minute Group Discussion (4:00 PM - 4:30 PM)**  
   The class will engage in a detailed discussion of the broader implications of hormone therapy on immune function. This will include a review of gender-specific immune adaptations during and after treatment, with consideration of how these changes may impact health outcomes in gender-diverse populations.

3. **Team Task: Confounding Variables and Gender in Immune Responses (4:30 PM - 5:15 PM) 💬**

### Hypothetical Study: Vaccine Efficacy in an Influenza Vaccine Trial
> **Study Design:**
> Researchers are conducting a clinical trial to assess the efficacy of a new influenza vaccine in preventing flu infections among adults aged 18–65. The trial includes 1,000 participants, randomly divided into two groups:
      Group 1 receives the new influenza vaccine.
      Group 2 receives a placebo. The primary outcome of interest is the vaccine efficacy, measured by the reduction in flu infections among vaccinated individuals compared to the placebo group.

## Questions:

## Do you control for gender, and how should you account for gender variability in a vaccine efficacy study?

> In your study on influenza vaccine efficacy, would you treat gender as a confounding variable that needs to be controlled, or as a primary variable of interest to account for in your analysis?
> > Controlling: What are the advantages and limitations of this approach in understanding the vaccine’s overall efficacy?
> > Accounting: What are the benefits of this approach in terms of understanding gender-specific immune responses?

## How can accounting for gender variability improve the understanding of vaccine efficacy and health outcomes?

> In the context of your vaccine efficacy study, how would disaggregating data by gender help reveal important differences in how males and females respond to the vaccine?

## What are the potential dangers of controlling for gender without fully acknowledging its importance in vaccine efficacy?

> Can you think of scenarios where simply controlling for gender—without examining its biological and immunological significance—could lead to misleading conclusions?

---

### Definition of cofounding variable (ref. Shapiro, Klein and Morgan, 2021)
> A confounding variable is a risk factor for the outcome that is also associated with the predictor, such that the observed relationship between predictor and outcome is confused by the presence of the confounder.

![Gender and Sex Variables](https://github.com/atomiclaboratory/systems_immunology_course_2024/blob/main/Course%20Materials/MODULE%203%20-%20Weeks%204-6/team%203%20Lynn%20Margulis/reading%20materials/Gender%20and%20sex%20variables.png)

*Figure adapted from: Shapiro JR, Klein SL, Morgan R. Stop ‘controlling’ for sex and gender in global health research. BMJ Global Health 2021;6:e005714. doi:10.1136/bmjgh-2021-005714*

---

### 📖 **Relevant Reading Materials on Confounding Variables and Gender in Research:**

1. **Stop ‘controlling’ for sex and gender in global health research**  
   - *Shapiro, Klein, and Morgan (2021)* argue that controlling for sex and gender can lead to misleading conclusions and advocate for disaggregating data to explore sex and gender as key variables.  
   [Link to Article](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC8048018/pdf/bmjgh-2021-005714.pdf)

2. **Sex differences in immune responses**  
   - *Nat Rev Immunol (2016)* provides an in-depth review of how sex differences influence immune responses, explaining why gender must be considered in immunological research.  
   [Link to Paper](https://www.nature.com/articles/nri.2016.90)

3. **Sex Differences in Immunity: Implications for the Development of Novel Vaccines Against Emerging Pathogens**  
   - *Anahita Fathi, Marylyn M. Addo, Christine Dahlke (2021)* explores how sex differences impact vaccine development and response, particularly in the context of emerging pathogens.  
   [Link to Article](https://www.frontiersin.org/journals/immunology/articles/10.3389/fimmu.2020.601170/full)

4. **How to Consider Gender in Health Research**  
   - *"Sex and gender in health research: updating policy to reflect evidence"*  
     This paper outlines strategies for properly incorporating sex and gender differences in health research.  
     [Link to Paper](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7027556/pdf/MJA2-212-57.pdf)

---

## 📊 Available Tools for Controlling or Accounting for Gender in Research

### **Controlling for Gender as a Confounding Variable:**

1. **Multiple Linear or Logistic Regression**  
   Include gender as a covariate in the regression model to control for its influence on the outcome. This isolates the relationship between the main predictor and the outcome.

2. **ANCOVA (Analysis of Covariance)**  
   ANCOVA can adjust for gender by treating it as a covariate, allowing the comparison of group outcomes while controlling for gender differences.

---

### **Accounting for Gender as a Variable of Interest:**

1. **Disaggregated Analysis**  
   Run separate analyses for different gender groups to examine how outcomes differ by gender, providing a clearer understanding of gender-specific effects.

2. **Mixed-Effects Models**  
   Include gender as both a fixed effect and a random effect to account for gender differences while also modeling individual variations in longitudinal or hierarchical data.

3. **Supervised Classification Models**  
   When using any supervised classification model (e.g., Random Forest, Support Vector Machines, Naive Bayes) with gender as a predictor, you account for gender by including it in the model. If gender does not show up as an important predictor (i.e., it has a low variable importance score or coefficient), this means the model does not find gender to significantly impact the outcome. In this case, you have **accounted** for gender but not explicitly **controlled** for it. Including gender allows the model to evaluate its potential role in influencing the outcome (e.g., vaccine efficacy), but if its importance is low, the data suggests that gender may not be a critical factor in this specific instance.

---