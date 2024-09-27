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
   
   **What is a Confusion Matrix?**  
   A confusion matrix is a tool used to evaluate the performance of a classification model. It shows the number of correct and incorrect predictions across the different classes in a dataset. The matrix consists of:
   
   - **True Positives (TP):** Correctly predicted positive cases.
   - **True Negatives (TN):** Correctly predicted negative cases.
   - **False Positives (FP):** Incorrectly predicted positive cases (also called Type I errors).
   - **False Negatives (FN):** Incorrectly predicted negative cases (also called Type II errors).

   **Confusion Matrix Example**  
   ![Confusion Matrix Example](https://github.com/atomiclaboratory/systems_immunology_course_2024/blob/main/Course%20Materials/MODULE%203%20-%20Weeks%204-6/team%202%20Sydney%20Brenner/model%20performance%20evaluation/confusion%20matrix%20example.jpg)

   **Understanding Sensitivity, Specificity, and Accuracy - Example**  
   To better understand how accuracy alone might not capture a model's true performance, especially with imbalanced data, here is an example using a spam detector model:
   
   ![Specificity and Sensitivity Example](https://github.com/atomiclaboratory/systems_immunology_course_2024/blob/main/Course%20Materials/MODULE%203%20-%20Weeks%204-6/team%202%20Sydney%20Brenner/model%20performance%20evaluation/specificity%20and%20sensitivity%20explained.jpg)

   ## **⚠️Question 1:** Why does this model have a high accuracy but poor performance in detecting spam? Which measurements would be more informative in this case?

   ##  **🔬Question 2:** Should Biological Data Be Evaluated with Accuracy or Sensitivity/Specificity?

   > **Answer:** The evaluation metric used for biological data depends on several factors, including the **type of data**, the **problem being solved**, and the **class distribution**. For most biological data, especially when the data are imbalanced or the stakes of incorrect predictions are high (e.g., disease diagnosis, vaccine response prediction), **sensitivity and specificity** are preferred over accuracy. 
   
   > **1. When to Use Accuracy:**
      > > -   **Balanced Data**: If the dataset has an equal or nearly equal number of samples across different classes (e.g., immune responses are evenly distributed between “high” and “low”), accuracy might be a useful metric. It gives a general overview of how well the model performs across all classes.
   > > -   **Low Cost of Misclassification**: If the consequences of a wrong prediction are relatively low (e.g., not detecting a mild immune response), accuracy could still be acceptable.
   > > However, **biological datasets are often imbalanced**, making accuracy less reliable in many cases.

   > **2. When to Use Sensitivity and Specificity:**
   > > -   **Imbalanced Data**: Biological data often have imbalanced classes, where one outcome (e.g., rare diseases, certain immune responses, pathogen detection) is much rarer than others. In these cases, **accuracy can be misleading** because it may show a high value simply due to the model’s ability to predict the dominant class well.
   > > -   **Sensitivity** (Recall) is critical when **focusing on detecting rare events** (e.g., identifying individuals who have a rare immune response or detecting a specific virus). Sensitivity evaluates how well the model captures positive cases, which can be extremely important in fields like disease detection or immune response analysis.
   > > -   **Specificity** is important when it’s crucial to **minimize false positives** (e.g., diagnosing a disease when it’s not present). In many biological cases, especially in screening tests, you want to avoid false positives as much as false negatives.

   > **3. What It Depends On:**
   > > -   **The Nature of the Problem**: In vaccine trials, for example, if the goal is to identify individuals with a strong immune response, **sensitivity** would be more important. If you are screening for a condition (like detecting a specific pathogen or disease), balancing **sensitivity** (catching all positives) and **specificity** (minimizing false alarms) is crucial.
   > > -   **Class Distribution**: If biological data are highly imbalanced, accuracy might paint an inaccurate picture of the model’s performance, so it’s better to focus on sensitivity and specificity.
   > > -   **Cost of False Positives/Negatives**: In some biological applications (e.g., cancer detection, autoimmune disease diagnosis), the cost of false positives or false negatives can be significant, so **sensitivity and specificity** provide a clearer evaluation of the model’s performance than accuracy.

   **Tools and Algorithms 🔧:**
   - *Precision-Recall Curves* (scikit-learn): [Guide](https://scikit-learn.org/stable/auto_examples/model_selection/plot_precision_recall.html)
   - *AUC-ROC Score* (scikit-learn): [AUC-ROC Example](https://scikit-learn.org/stable/auto_examples/model_selection/plot_roc_crossval.html)
   - *Confusion Matrix* (scikit-learn): [Guide](https://scikit-learn.org/stable/auto_examples/model_selection/plot_confusion_matrix.html)

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