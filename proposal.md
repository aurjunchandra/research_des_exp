# Project Proposal: Student Dropout Risk Prediction 2026

## 1. Introduction

Student dropout is a significant challenge for educational institutions. Students may discontinue their education for various reasons, including academic difficulties, financial challenges, and other personal or institutional factors. Identifying students who may be at risk of dropping out can help institutions provide timely academic guidance and support.

This project proposes a machine learning classification system to predict student dropout risk using publicly available student data. The project will follow a structured data science workflow, including data exploration, preprocessing, model training, evaluation, and interpretation.

## 2. Research Question

**Can machine learning classification algorithms predict student dropout risk from available student academic, enrollment, and related characteristics?**

The project will also investigate which available features are most strongly associated with dropout predictions and compare the predictive performance of two classification algorithms.

## 3. Dataset and Source

**Dataset name:** Student Dropout Prediction Challenge

**Source:** Kaggle

**Dataset link:** https://www.kaggle.com/competitions/studentdropout/data

**Dataset type:** Structured/tabular data

**Machine learning technique:** Supervised learning — classification

The dataset provides student retention information and dropout labels for a prediction task. Access to the competition data may require accepting the competition rules or obtaining an invitation.

Before modeling, the downloaded files, target labels, feature definitions, missing values, and class distribution will be inspected. The analysis will use only features that are available and appropriate for the prediction task.

If the Kaggle competition data cannot be accessed, the alternative will be the UCI Machine Learning Repository dataset:

https://archive.ics.uci.edu/dataset/697/predict+students+dropout+and+academic+success

The UCI dataset contains 4,424 student records, 36 features, and three outcome categories: Dropout, Enrolled, and Graduate. If this alternative is used, the target definition and any conversion to a binary classification task will be documented explicitly.

## 4. Literature Review: Two-Source Scan

### Source 1

Villar, A., & de Andrade, C. R. V. (2024). *Supervised machine learning algorithms for predicting student dropout and academic success: A comparative study.*

Link: https://link.springer.com/article/10.1007/s44163-023-00079-z

This study compares supervised machine learning algorithms for predicting student dropout and academic success. It discusses models such as Decision Tree, Support Vector Machine, Random Forest, and boosting algorithms. It also addresses class imbalance, which can affect dropout prediction.

**Relevance to this project:** The study supports comparing multiple classification algorithms and considering class imbalance when evaluating student dropout predictions.

### Source 2

Romero, S., & Liao, X. (2025). *Statistical and machine learning models for predicting university dropout and scholarship impact.* PLOS ONE, 20(6), e0325047.

Link: https://doi.org/10.1371/journal.pone.0325047

This research analyzes university dropout using data from 4,424 students. It investigates statistical and machine learning approaches and examines the relationship between student characteristics, scholarships, and dropout outcomes. The authors emphasize interpretability and acknowledge limitations associated with studying one institution and one period.

**Relevance to this project:** This research motivates the use of transparent models, careful interpretation of predictors, and recognition that model results may not generalize to every educational institution.

## 5. Research Gap and Proposed Contribution

Existing research demonstrates that machine learning can support student dropout prediction. However, model performance depends on the dataset, target definition, feature availability, and evaluation strategy.

This project will implement a reproducible classification workflow and compare Logistic Regression with Random Forest on the selected dataset. It will report the evaluation results transparently rather than assume that one model will perform best in advance.

## 6. Proposed Methodology

1. Load the selected public dataset and inspect its structure.
2. Explore feature types, missing values, duplicate records, and target distribution.
3. Preprocess numerical and categorical features using appropriate transformations.
4. Split the data into training and testing sets, using stratification where appropriate.
5. Train a Logistic Regression classifier.
6. Train a Random Forest classifier.
7. Evaluate both models using accuracy, precision, recall, F1-score, ROC-AUC where appropriate, and a confusion matrix.
8. Compare the results and investigate important predictive features.
9. Document limitations, ethical considerations, and possible improvements.

All preprocessing steps will be fitted on the training data only to reduce data leakage. Class imbalance will be assessed, and any resampling will be restricted to training data.

## 7. Expected Outcome

The expected outcome is a reproducible machine learning project that demonstrates how classification models can be used to estimate student dropout risk. The project will provide a comparison of two models and identify patterns in the selected dataset that may help inform student support strategies.

The system will be treated as a decision-support experiment, not as a definitive judgment about any individual student.

## 8. Tools and Technologies

- Python
- Pandas and NumPy
- Matplotlib and Seaborn
- Scikit-learn
- Jupyter Notebook or VS Code
- Git and GitHub

## 9. Ethical Considerations and Limitations

Student data may contain sensitive or potentially biased characteristics. The project will use publicly available data, avoid unnecessary disclosure of individual records, and discuss fairness, privacy, and limitations. Predictions must not be used as the sole basis for denying educational opportunities or making consequential decisions about students.

The dataset may represent a particular institution or population, so the model's performance may not generalize to other educational settings.

## 10. References

1. Villar, A., & de Andrade, C. R. V. (2024). Supervised machine learning algorithms for predicting student dropout and academic success: A comparative study. https://link.springer.com/article/10.1007/s44163-023-00079-z

2. Romero, S., & Liao, X. (2025). Statistical and machine learning models for predicting university dropout and scholarship impact. PLOS ONE, 20(6), e0325047. https://doi.org/10.1371/journal.pone.0325047

3. Kaggle. Student Dropout Prediction Challenge. https://www.kaggle.com/competitions/studentdropout/data

4. UCI Machine Learning Repository. Predict Students' Dropout and Academic Success. https://archive.ics.uci.edu/dataset/697/predict+students+dropout+and+academic+success