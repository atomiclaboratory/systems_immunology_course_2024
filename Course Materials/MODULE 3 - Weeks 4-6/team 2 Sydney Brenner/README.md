# 🌬️🦠 Decoding Influenza Vaccination: Systems Biology Insights

## Team 2 - Sydney Brenner

**Members:**
- Ziqing Yu  
- Erica Anton  
- Annelisa Fache

This team will analyze the systems biology approach to influenza vaccination, discussing early molecular signatures that can predict vaccine efficacy. Their presentation will focus on the comparison between the trivalent inactivated influenza vaccine (TIV) and the live attenuated influenza vaccine (LAIV), highlighting the role of systems biology in understanding these differences.

---

## Presentation Overview

**Topic:** *Systems biology of vaccination for seasonal influenza in humans*  
**Paper Reference:**  
- Helder I Nakaya, Jens Wrammert, Eva K Lee, Luigi Racioppi, Stephanie Marie-Kunze, W Nicholas Haining, Anthony R Means, Sudhir P Kasturi, Nooruddin Khan, Gui-Mei Li, Megan McCausland, Vibhu Kanchan, Kenneth E Kokko, Shuzhao Li, Rivka Elbein, Aneesh K Mehta, Alan Aderem, Kanta Subbarao, Rafi Ahmed & Bali Pulendran  
- *Nature Immunology*, volume 12, pages 786–795 (2011)  
- [Link to Paper](https://www.nature.com/articles/ni.2067)

### Abstract Summary 📄

This study uses a systems biology approach to investigate both innate and adaptive immune responses to influenza vaccines in humans over three consecutive influenza seasons. The authors examined healthy adults receiving either the trivalent inactivated influenza vaccine (TIV) or the live attenuated influenza vaccine (LAIV). Their findings show that TIV induced higher antibody titers and more plasmablasts compared to LAIV. Furthermore, early molecular signatures were identified that could predict later antibody responses, with the kinase CaMKIV emerging as a regulator of these responses. These results demonstrate how systems biology can be employed to predict vaccine immunogenicity and uncover new mechanisms behind vaccine efficacy.

---

## Activities 📚

1. **30-Minute Presentation by Team Brenner (Until 4:00 PM)**  
   Team Brenner will present their analysis of the *Nature Immunology* paper, focusing on the systems biology approach and its role in predicting vaccine efficacy, as well as the comparative analysis of TIV and LAIV vaccines.

2. **30-Minute Group Discussion (4:00 PM - 4:30 PM)**  
   The class will engage in a detailed discussion of the findings, the significance of early molecular signatures, and the practical implications for improving influenza vaccines.

3. **Team Tasks: Post-Presentation Discussion (4:30 PM - 5:15 PM) 💬**

   ## 3A: Is accuracy the best way to evaluate the model? Why not?

   **Discussion points:**
   - Accuracy might be misleading when dealing with imbalanced data (e.g., more individuals with high responses). In such cases, metrics like precision, recall, and AUC-ROC can provide a better understanding of the model’s predictive power.
   - Precision-Recall curves and AUC-ROC are better alternatives for evaluating vaccine efficacy prediction models.
   
   **Tools and Algorithms 🔧:**
   - *Precision-Recall Curves* (scikit-learn): [Guide](https://scikit-learn.org/stable/auto_examples/model_selection/plot_precision_recall.html)
   - *AUC-ROC Score* (scikit-learn): [AUC-ROC Example](https://scikit-learn.org/stable/auto_examples/model_selection/plot_roc_crossval.html)
   - *Confusion Matrix* (scikit-learn): [Guide](https://scikit-learn.org/stable/auto_examples/model_selection/plot_confusion_matrix.html)

   **What is a Confusion Matrix?**  
   A confusion matrix is a tool used to evaluate the performance of a classification model. It shows the number of correct and incorrect predictions across the different classes in a dataset. The matrix consists of:
   
   - **True Positives (TP):** Correctly predicted positive cases.
   - **True Negatives (TN):** Correctly predicted negative cases.
   - **False Positives (FP):** Incorrectly predicted positive cases (also called Type I errors).
   - **False Negatives (FN):** Incorrectly predicted negative cases (also called Type II errors).

   **Confusion Matrix Example**  
   ![Confusion Matrix Example](https://github.com/atomiclaboratory/systems_immunology_course_2024/blob/main/Course%20Materials/MODULE%203%20-%20Weeks%204-6/team%202%20Sydney%20Brenner/confusion%20matrix/confusion%20matrix%20example.jpg)

   **Understanding Sensitivity, Specificity, and Accuracy - Example**  
   To better understand how accuracy alone might not capture a model's true performance, especially with imbalanced data, here is an example using a spam detector model:
   
   ![Specificity and Sensitivity Example](https://github.com/atomiclaboratory/systems_immunology_course_2024/blob/main/Course%20Materials/MODULE%203%20-%20Weeks%204-6/team%202%20Sydney%20Brenner/model%20performance%20evaluation/specificity%20and%20sensitivity%20explained.jpg)

   ---
   ***Why does this model have a high accuracy but poor performance in detecting spam?***
   ---

   **Relevant Reading 📖:**
   - *A Survey of Model Evaluation Metrics for Imbalanced Data Classification*: [Paper Link](https://arxiv.org/abs/1505.01658)

   ## 3B: Why do the authors focus only on validating one gene? How would you run the analysis to capture more systems-level understanding of vaccine responses? Which approaches?

   **Discussion points:**
   - Authors validated CaMKIV due to its biological relevance, but this may limit the broader understanding of immune responses. A systems-level approach, integrating multi-omics and pathway analysis, provides a more comprehensive view.
   - Tools like GSEA or Network analysis can uncover more complex interactions between multiple genes and pathways.
   
   **Tools and Approaches 🔧:**
   - *Reactome* (Pathway database): [Access Reactome](https://reactome.org/)
   - *Gene Set Enrichment Analysis (GSEA)*: [GSEA Tool](https://www.gsea-msigdb.org/gsea/index.jsp)
   - *GeneTonic* (GSEA and sGSEA in R): [GeneTonic R package](https://bioconductor.org/packages/release/bioc/html/GeneTonic.html)
   - *Cytoscape* (Network analysis): [Cytoscape Tool](https://cytoscape.org/)
   - *Clinical Knowledge Graph (CKG)* (Network analysis): [CKG Tool](https://ckg.readthedocs.io/en/latest/INTRO.html)

   **Relevant Reading 📖:**
   - *Gene Set Enrichment Analysis*: [GSEA Paper](https://www.pnas.org/content/102/43/15545)
   - *Clinical Knowledge Graph*: [CKG Paper](https://www.nature.com/articles/s41587-021-01145-6)