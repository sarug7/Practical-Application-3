# Practical-Application-3


## Project Overview
This repository contains my submission for **Required Assignment 17.1: Comparing Classifiers**.  
The goal of this project is to compare multiple classification algorithms on a bank marketing dataset and evaluate their performance using appropriate metrics for an imbalanced classification problem.

The analysis is conducted in a Jupyter Notebook and follows the **CRISP-DM methodology**, with a clear focus on business understanding, modeling, evaluation, and actionable insights.

---

## Business Understanding
The business objective is to **improve the efficiency of a bank’s direct marketing campaigns** by predicting whether a client will subscribe to a term deposit.  
By identifying clients with a higher likelihood of subscription, the bank can:
- Reduce unnecessary customer contacts
- Lower call-center costs
- Allocate marketing resources more effectively

## Repository Structure
```
.
├── prompt_III.ipynb        # Main Jupyter Notebook 
├── data                    # data files
├── README.md               # Project documentation
```


## Jupyter Notebook
📓 **Notebook:** [`prompt_III.ipynb`](prompt_III.ipynb)


## Data & Preparation
- Dataset: UCI Bank Marketing Dataset
- Target variable: `y` (term deposit subscription: yes/no)
- Missing values and encoded placeholders (`unknown`, sentinel values) are handled explicitly
- Features are encoded appropriately for machine learning models
- Data is split into stratified training and test sets



## Models Compared
The following classifiers are implemented and compared:

- Dummy Classifier (baseline)
- Logistic Regression
- K-Nearest Neighbors (KNN)
- Decision Tree
- Support Vector Machine (SVM)

Model comparison includes:
- Training time
- Training accuracy
- Test accuracy
- ROC-AUC (primary evaluation metric)

Cross-validation and grid search are used to tune hyperparameters where appropriate.

---

## Evaluation Metrics
Because the dataset is highly imbalanced, **ROC-AUC** is used as the primary evaluation metric, supported by:
- Accuracy
- Precision
- Recall
- F1-score

The rationale for this choice is clearly explained in the notebook, with an emphasis on business impact rather than raw accuracy.

---

## Visualizations
The notebook includes:
- Plots for categorical and continuous variables
- ROC curves and Precision–Recall curves for model comparison



## Key Findings
- The Dummy Classifier achieves high accuracy due to class imbalance but provides no business value.
- Logistic Regression offers a strong balance of interpretability, performance, and training speed.
- Decision Trees show signs of overfitting without tuning.
- SVM achieves strong discrimination but with higher computational cost.
- ROC-AUC and recall are more informative than accuracy for this problem.

---

## Recommendations & Next Steps
- Tune classification thresholds to balance recall and precision based on business cost
- Incorporate additional pre-contact features if available
- Explore ensemble methods for further performance gains
- Collaborate with business stakeholders to define cost-sensitive evaluation metrics

---

## Tools & Libraries
- Python
- pandas, numpy
- scikit-learn
- matplotlib, seaborn

---

## Summary
This project demonstrates a structured and interpretable approach to comparing classifiers on an imbalanced dataset. By focusing on appropriate evaluation metrics and clear business objectives, the analysis delivers insights that are actionable for a nontechnical audience.

---

**Author:** Uma  
**Assignment:** Required Assignment 17.1 – Comparing Classifiers
