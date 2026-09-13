# Business_Intelligence_Analytics

# Lending Club Credit Risk Analysis using CART

## Project Overview

This project was developed as part of a Business Intelligence & Analytics project to explore the application of Machine Learning to a real-world credit-risk dataset.

The project uses the Lending Club dataset to classify loans into two categories:

- Fully Paid
- Charged Off

The analysis includes Exploratory Data Analysis (EDA), data preprocessing, feature selection, and the development of a CART (Classification and Regression Tree) model.

The broader project involves comparing multiple Machine Learning techniques to determine which model provides the best performance for the dataset.

---

## Dataset

The dataset used in this project is the Lending Club dataset.

### Dataset Details

- Number of observations: 7,151
- Number of variables: 16
- Target variable: `loan_status`
- Target classes:
  - Fully Paid
  - Charged Off

The dataset contains borrower, loan and credit-history related variables such as:

- Loan amount
- Interest rate
- Installment
- Annual income
- Home ownership
- Verification status
- Revolving balance
- Revolving utilization
- Total accounts
- Accounts opened in the past 24 months

---

## Methodology

The analysis follows the following workflow:

1. Data loading and inspection
2. Exploratory Data Analysis (EDA)
3. Missing-value analysis
4. Duplicate-value check
5. Target-variable analysis
6. Feature selection
7. Data preprocessing
8. Categorical variable encoding
9. Train-test split
10. CART model development
11. Model prediction
12. Model evaluation
13. Confusion matrix analysis
14. Decision-tree visualization
15. Feature-importance analysis

An 80:20 stratified train-test split was used for model evaluation.

---

## CART Model

A Decision Tree Classifier was developed using the CART approach.

The model was configured using:

- Criterion: Gini impurity
- Maximum tree depth: 5
- Random state: 42

Categorical variables were converted using one-hot encoding, while missing numerical values were handled using median imputation.

---

## Model Performance

The CART model achieved the following results on the test dataset:

| Metric | CART |
|---|---:|
| Accuracy | 82.74% |
| Precision | 41.94% |
| Recall | 5.37% |
| F1 Score | 9.52% |

Although the model achieved an overall accuracy of 82.74%, its recall for the Charged Off class was only 5.37%.

This highlights an important issue in credit-risk modelling: **accuracy alone may not provide a complete picture of model performance when the target variable is imbalanced.**

The model correctly identified 13 of the 242 Charged Off loans in the test set.

---

## Key Learning

One of the main takeaways from this project was the importance of evaluating Machine Learning models using multiple performance metrics.

In a credit-risk context, identifying potentially risky loans can be more important than achieving a high overall accuracy.

Therefore, precision, recall and F1-score were considered alongside accuracy when evaluating the CART model.

---

## Technologies Used

- Python
- Google Colab
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Excel

---

## Repository Contents

| File | Description |
|---|---|
| `CART_Coding.ipynb` | Google Colab/Jupyter notebook containing the Python code, EDA, preprocessing, CART model and evaluation |
| `Lending Club dataset.xlsx` | Dataset used for the analysis |
| `BIA_NCP3_Project_Report.docx` | Project report containing the methodology, findings and business implications |

---

## Project Objective

The broader objective of the project is to apply three different Machine Learning techniques to the dataset and compare their performance using accuracy, precision, recall and F1-score to determine which technique best fits the data.

<img width="1541" height="1966" alt="01_eda_loan_status" src="https://github.com/user-attachments/assets/3486dc8a-bc03-40ac-8b92-c3576e510540" />
<img width="1541" height="1051" alt="02_eda_interest_rate" src="https://github.com/user-attachments/assets/21157e7b-7c11-4fce-974a-d70623ad959f" />
<img width="1541" height="2056" alt="03_cart_metrics" src="https://github.com/user-attachments/assets/d14e8924-1a5b-4830-a6da-9afa4b624d18" />
<img width="1541" height="1836" alt="04_cart_confusion_matrix" src="https://github.com/user-attachments/assets/807f95f3-04f6-41d0-ba8d-dd863b297ea5" />
<img width="1541" height="1006" alt="05_cart_decision_tree" src="https://github.com/user-attachments/assets/655934e1-3220-4084-82b0-f065368ec4f4" />

