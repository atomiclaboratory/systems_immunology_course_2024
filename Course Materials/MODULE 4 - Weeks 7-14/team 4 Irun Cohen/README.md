# Neural Networks and Regularization 🧠🔗
**Team 4 - Irun Cohen**

---

### 👥 Team Members
- Shea Mowry
- Han Kahvecioglu
- Maya Bartels
- Felipe Munoz
- Meghan Pinter

This team will dive into neural networks and their ability to model complex, non-linear relationships in immunological data. Emphasis will be placed on regularization techniques to prevent overfitting, enhance model generalization, and ensure reliability in predictions.

---

## 🌟 Class Activities

1. **Introduction to Neural Networks and Regularization (Until 4:00 PM) 🧠**
   - We’ll start with a presentation on neural networks and their use in supervised learning, specifically for immunological data.
   - The team will explain **neural network** and **multiple-layer perceptron** and discuss how these techniques help optimize models by reducing overfitting.

2. **Hands-on Neural Network Modeling with PANDORA (4:00 PM - 5:15 PM) 💻**
   - Apply neural network algorithms, **nnet** and **mlpWeightDecay**, and compare them to the four previously used algorithms: Naive Bayes, Linear Discriminant Analysis, Random Forest, and C5.0.
   - **Goal**: Train a model to predict who will be high or low responders 6 months post-COVID-19 infection, focusing on minimizing overfitting.

---

## 📊 Dataset Overview
- We’ll use the same dataset as in the last two classes. Download it from the ‘Dataset’ folder.

---

## 🧩 Concepts to Understand

### Overfitting 🔍
Overfitting occurs when a model learns the training data too well, capturing noise or irrelevant details, which reduces its ability to generalize to new data. This often leads to a high **Train AUC** but a lower **Predict AUC**.

### Underfitting 📉
Underfitting happens when a model is too simple to capture the underlying patterns in the data. It will show low performance on both the training and testing sets, leading to both low Train AUC and Predict AUC.

### Train AUC vs. Predict AUC 📈
**Train AUC** indicates the model's performance on the training set, while **Predict AUC** assesses its performance on the test set. High Train AUC and low Predict AUC usually indicate overfitting.

---

## 🎯 Team Tasks

### TASK 1: Algorithm Comparison 🔄
- **Objective**: Compare **nnet** and **mlpWeightDecay** with previously studied algorithms (**nb**, **lda**, **rf**, and **C5.0**).
- **Goal**: Identify which model performs best for predicting COVID-19 response at 6 months, and analyze which models may have overfitted.

### 📝 Quiz for Task 1:
**Join the Interactive Quiz on Slido**: [Slido Link](https://app.sli.do/event/vZQmBiVjSDaCwtayvC4fsw)

**Before analysis**:
- **Q1**: Based on your understanding of different algorithms and the COVID-19 dataset you have, which model would you expect to perform best, and why?
- **Q2**: When evaluating models, why is it important to look at both Train AUC and Predict AUC in addition to other metrics?

**After analysis**:
- **Q1**: Based on the results, which model performed best and why?
- **Q2**: Which models show signs of overfitting, and why?

---

### TASK 2: Impact of Data Partitioning on Model Performance 📊
- **Objective**: Test all six algorithms with different data partitioning methods to see how training dataset size affects performance.
  - **Partition 1**: 50% training (n=37) / 50% testing (n=37)
  - **Partition 2**: 80% training (n=61) / 20% testing (n=14)

### 📝 Quiz for Task 2
**Partition 1 (50% Training/50% Testing)**
- **Prediction**: What do you think will happen with a smaller training set (50%)?
- **Analysis**: Which models handled the reduced training data best, and why?

**Partition 2 (80% Training/20% Testing)**
- **Prediction**: What do you think will happen with a larger training set (80%)?
- **Analysis**: Which models improved most with more training data, and which continued to underperform?

---

### TASK 3: Effects of Preprocessing Steps on Model Performance 🧪
- **Objective**: Test all algorithms using 75%/25% partition, with modified preprocessing (only center/scale and median impute; no removal of correlated features,corr or low-variance features, zv/nzv).
  
### 📝 Quiz for Task 3 after analysis:
**Join the Interactive Quiz on Slido**: [Slido Link](https://app.sli.do/event/vZQmBiVjSDaCwtayvC4fsw)
- **Q1**: What impact do you expect from keeping correlated features?
- **Q2**: How might zero/near-zero variance features affect the models?
- **Q3**: Which models are most affected by correlated and low-variance features?
- **Q4**: How does including these features impact AUC and computation time?