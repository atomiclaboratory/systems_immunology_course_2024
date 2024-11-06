# Neural Networks and Regularization 🧠🔗
**Team 4 - Irun Cohen**

### Members:
- Shea Mowry
- Han Kahvecioglu
- Maya Bartels
- Felipe Munoz
- Meghan Pinter

This team will explore neural networks and their capability to model non-linear relationships within complex immunological datasets. They will emphasize the importance of regularization techniques to prevent overfitting and improve generalization, ensuring model reliability.

---

## Activities 📚

1. **Introduction to Neural Networks and Regularization (Until 4:00 PM) 🧠**
   - The team will present the fundamentals of neural networks, focusing on their use in supervised learning for immunology.
   - Discussion on regularization techniques, including LASSO and elastic net, to optimize model performance.

2. **Hands-on Neural Network Modeling with PANDORA (4:00 PM - 5:15 PM) 💻**
   - In this session, participants will apply neural network and regularization methods to immunological datasets to predict outcomes, using PANDORA as the analytical platform.
   - **Goal**: Achieve a model that predicts complex immunological responses with minimized overfitting.

---

## 📊 Dataset Overview

The dataset includes variables that reflect immune response measurements, including antibody titers, T-cell responses, and cytokine levels. Key variables have been selected to capture the diversity in immune response patterns and individual variability.

- **Antibody measures**: IgA, IgG, IgM levels across different pathogens
- **T-Cell Responses**: CD8+ and CD4+ responses in various stimulation contexts
- **Cytokine Levels**: Indicators of inflammatory and anti-inflammatory responses
- **Outcome Variable**: **Immunological Outcome** – Predicted likelihood of a strong immune response based on baseline data

---

## ML Analysis Parameters

- **Outcome**: **Immunological Outcome**
   - Target variable representing the likelihood of a strong immune response.
   
- **Predictors**: All measurements excluding demographic variables.
   - Immunological measurements serve as input features in the neural network model.

- **Training Set**: 75% of the data
   - Used for model training and tuning of parameters.

- **Test Set**: 25% of the data
   - Used for evaluating model generalization to unseen data.

---

## Preprocessing

1. **Centering and Scaling**:
   - Standardizes data to ensure all features contribute equally to the neural network.

2. **Median Imputation**:
   - Replaces missing values with the column median for robust handling of missing data.

3. **Feature Selection with Regularization**:
   - Reduces feature redundancy and improves model efficiency through LASSO or elastic net.

---

## Team Tasks

- **Comparison of nnet and mlpWeightDecay**: How do Neural Networks and Multilayer Perceptrons with Weight Decay differ in their predictive power and interpretability?
- **Algorithm Comparison**: Compare nnet and mlpWeightDecay to linear models used in prior classes; discuss where neural networks provide advantages in handling complex, non-linear data.
- **Regularization Impact**: Evaluate the impact of regularization on model performance, focusing on preventing overfitting.

---

## Self-Paced Analysis Tasks ⏳

For those interested in deeper exploration:

1. **Explore Regularization Variants**:
   - Compare results of different regularization techniques, such as ridge regression, LASSO, and elastic net, to see their effects on the model’s stability.

2. **Network Architecture Exploration**:
   - Experiment with varying hidden layers and nodes to see how model complexity affects predictions and generalizability.

These tasks allow further investigation into the flexibility and challenges of neural networks in immunology data modeling.
