# Research Methodology
## Student Dropout Risk Prediction — 2026

### 1. Refined Research Question

Can student academic performance, enrollment information, demographic characteristics, and socioeconomic factors predict whether a higher education student will Dropout, remain Enrolled, or Graduate?

The project aims to compare Logistic Regression and Random Forest to identify an effective classification model for predicting student academic outcomes.

### 2. Dataset Description

**Dataset Name:** Predict Students' Dropout and Academic Success

**Source:** UCI Machine Learning Repository

**Dataset URL:** https://archive.ics.uci.edu/dataset/697/predict+students+dropout+and+academic+success

**Dataset Characteristics:**
- Total records: 4,424
- Input features: 36
- Target variable: Target
- Data type: Numerical, categorical, and integer
- Machine learning task: Multiclass classification

**Target Classes:**
- Dropout
- Enrolled
- Graduate

**Feature Categories:**

1. Enrollment information: Application mode, application order, course, attendance, and previous qualification.
2. Demographic information: Age, gender, nationality, and marital status.
3. Socioeconomic information: Parents' qualifications and occupations, scholarship status, and tuition fee status.
4. Academic information: First-semester curricular units, approved units, evaluations, and grades.

**Dataset Limitations:**

- The dataset represents students from a particular higher education institution in Portugal.
- The dataset may not generalize to every educational institution or country.
- The target classes are imbalanced.
- Some features are institution-specific.
- The dataset is relatively small compared with large-scale educational datasets.

### 3. Data Cleaning Plan

The following preprocessing steps will be applied:

1. Load the CSV dataset using Pandas.
2. Examine the dataset dimensions and column names.
3. Check missing values and duplicate records.
4. Inspect data types and invalid values.
5. Separate input features and target variable.
6. Exclude second-semester academic performance features to reduce future-information leakage when predicting outcomes after the first semester.
7. Apply appropriate preprocessing to numerical and categorical features.

### 4. Feature Engineering Plan

The following features will be used:

- Enrollment-related information.
- Demographic information.
- Socioeconomic information.
- Previous academic qualifications.
- First-semester academic performance.

Feature preprocessing:

- Numerical features: StandardScaler.
- Categorical features: OneHotEncoder.
- Missing numerical values: Median imputation if necessary.
- Missing categorical values: Most frequent imputation if necessary.

A ColumnTransformer and Pipeline will be used to apply preprocessing consistently.

### 5. Model Selection

Two classification algorithms will be implemented.

**Model 1: Logistic Regression**

Logistic Regression will be used as the baseline classification model. It is computationally efficient, relatively easy to interpret, and suitable for multiclass classification.

**Model 2: Random Forest Classifier**

Random Forest combines multiple decision trees to capture nonlinear relationships and interactions between student characteristics. It can handle complex tabular data and provides feature-importance information.

Both models will use class weighting where appropriate to address class imbalance.

### 6. Train-Test Split

The dataset will be divided into:

- Training data: 80%
- Testing data: 20%

The split will use stratification to maintain the distribution of target classes.

Random state: 42.

### 7. Evaluation Metrics

The following evaluation metrics will be used:

**Accuracy:** Measures the proportion of correctly classified students.

**Precision:** Measures how many predicted cases of a particular class are correct.

**Recall:** Measures how many actual cases of a particular class are correctly identified. Dropout-class recall is particularly important.

**F1-score:** Balances precision and recall.

**Macro F1-score:** Calculates the average F1-score across all classes, giving each class equal importance.

**Confusion Matrix:** Shows correct and incorrect predictions for each class.

**ROC-AUC:** Measures classification performance across different decision thresholds using a one-vs-rest multiclass approach.

Macro F1-score and Dropout-class recall will receive particular attention because the dataset has imbalanced target classes.

### 8. Experimental Procedure

1. Load and inspect the dataset.
2. Clean the data.
3. Engineer and preprocess features.
4. Split the dataset into training and testing sets.
5. Train Logistic Regression.
6. Train Random Forest.
7. Evaluate both models using the selected metrics.
8. Compare their performance.
9. Identify important predictive features.
10. Discuss findings and limitations.

### 9. Expected Outcome

The experiment is expected to identify which classification algorithm performs better in predicting student academic outcomes. The results may help demonstrate how machine learning can support early identification of students who need additional academic assistance.

### 10. Ethical Considerations

Predictions should be used to provide supportive interventions rather than punish or discriminate against students. Student privacy, data protection, model bias, and fairness should be considered before applying any predictive system in real educational institutions.