# Credit Risk Analysis & Predictive Modeling

A machine learning project focused on analyzing borrower characteristics and predicting loan credit risk using multiple classification algorithms.

## 📌 Project Overview

Credit risk assessment is an important task in the lending industry. The goal of this project is to analyze borrower and loan-related information and build machine learning models that can classify whether a loan is likely to be associated with a higher credit risk.

The project follows a complete data science workflow:

- Exploratory Data Analysis (EDA)
- Data cleaning and preprocessing
- Feature analysis
- Categorical encoding
- Feature scaling
- Model development
- Model evaluation
- Model comparison
- Feature importance analysis

## 🎯 Objective

The main objectives of this project are to:

- Understand the factors associated with loan status
- Explore patterns in borrower and loan characteristics
- Prepare the dataset for machine learning
- Build and compare multiple classification models
- Evaluate models using appropriate classification metrics
- Identify important features contributing to credit-risk prediction

## 📊 Dataset

The dataset contains **32,581 records and 12 columns** describing borrower and loan characteristics.

### Features

| Feature | Description |
|---|---|
| `person_age` | Age of the borrower |
| `person_income` | Annual income |
| `person_home_ownership` | Home ownership status |
| `person_emp_length` | Employment length |
| `loan_intent` | Purpose of the loan |
| `loan_grade` | Loan grade |
| `loan_amnt` | Loan amount |
| `loan_int_rate` | Loan interest rate |
| `loan_status` | Target variable |
| `loan_percent_income` | Loan amount as a percentage of income |
| `cb_person_default_on_file` | Historical default indicator |
| `cb_person_cred_hist_length` | Length of credit history |

### Target Variable

`loan_status`

- `0` → Non-default / lower-risk class
- `1` → Default / higher-risk class

The dataset contains approximately **78.18% class 0** and **21.82% class 1**, making class distribution an important consideration during model evaluation.

## 🔍 Exploratory Data Analysis

The project includes:

- Dataset structure and statistical analysis
- Missing-value analysis
- Duplicate-record analysis
- Target-variable distribution
- Numerical feature distributions
- Boxplots for numerical variables
- Correlation analysis
- Categorical feature analysis
- Feature relationships with the target variable

The dataset initially contained missing values in:

- `person_emp_length`
- `loan_int_rate`

These missing values were handled using median imputation.

## ⚙️ Data Preprocessing

The following preprocessing steps were performed:

1. Missing-value identification
2. Median imputation for numerical missing values
3. Identification of categorical features
4. Label encoding of categorical variables
5. Separation of features and target
6. Stratified train-test split
7. Standard scaling of features

### Train-Test Split

- Training set: **26,064 records**
- Testing set: **6,517 records**
- Test size: **20%**
- Random state: `42`
- Stratification: Applied using the target variable

## 🤖 Machine Learning Models

Four classification approaches were explored:

### 1. Logistic Regression

Used as a baseline classification model.

### 2. Decision Tree

Used to capture non-linear relationships between borrower characteristics and loan status.

### 3. Random Forest

An ensemble learning method using multiple decision trees to improve predictive performance.

### 4. XGBoost

A gradient-boosting based model used for advanced classification and feature importance analysis.

## 📈 Model Evaluation

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC
- Confusion Matrix
- ROC Curve

Because the target classes are imbalanced, metrics such as **Precision, Recall, F1 Score, and ROC-AUC** are considered alongside accuracy.

## 📊 Verified Model Results

The following results are directly recorded from the executed notebook outputs.

| Model | Accuracy | Precision | Recall | F1 Score | ROC-AUC |
|---|---:|---:|---:|---:|---:|
| Logistic Regression | 84.49% | 72.41% | 46.69% | 56.78% | 85.16% |
| Decision Tree | 89.17% | 74.62% | 76.30% | 75.45% | 84.53% |
| Random Forest | 93.19% | 96.84% | 71.10% | 82.00% | 92.85% |

The notebook also contains an XGBoost model and a model-comparison section. Its final evaluation outputs should be regenerated when reproducing the notebook before treating those values as final reported results.

## 🔎 Feature Importance

XGBoost feature importance is used to investigate which input variables contribute most strongly to the model's predictions.

The project generates a feature-importance analysis and visualization to support interpretation of the predictive model.

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- XGBoost
- Joblib
- Jupyter Notebook / Google Colab

## 📁 Project Structure

```text
credit-risk-analysis/
│
├── Credit_Risk_Analytics_and_Predictive_Modeling.ipynb
├── README.md
└── data/
    └── credit_risk_dataset.csv
