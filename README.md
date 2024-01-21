#### credit-risk-classification Challenge
# Analysis of Logistic Regression Models for Loan Prediction

### Purpose of the Analysis:
The analysis aims to predict loan status (healthy or non-healthy) based on various financial features using logistic regression. Two scenarios are considered: one with the original data and another with oversampled data to address class imbalance.

### Financial Information:
The dataset (lending_data.csv) contains financial information related to loans, including features like loan size, interest rate, borrower income, debt-to-income ratio, number of accounts, derogatory marks, and total debt. The goal is to predict the loan status, where 0 represents a healthy loan and 1 represents a non-healthy loan.

### Stages of Machine Learning Process:
1. Data Preparation:
Loaded the dataset and reviewed the data's overall summary. Labels (y) and features (X) were then created from the dataset.
2. Data Splitting:
The data was split into training and testing sets using train_test_split.
3. Created a logistic regression model with the original data.
Fitted the model using training data and made predictions on the test set.
Evaluated the model's performance using accuracy, confusion matrix, and classification report.
4. RandomOverSampler was used to address class imbalance in the training data.
logistic regression model was created with the oversampled data.
The model was fitted and predictions were done on the test set.
Evaluated the model's performance using accuracy, confusion matrix, and classification report.


### Logistic Regression Model Evaluation (Original Data)

#### Label 0 (Healthy Loan):
- **Precision (pre):** 1.00
  - Identifies all predicted healthy loans correctly.
- **Recall (rec):** 0.99
  - Correctly identifies 99% of actual healthy loans.
- **Specificity (spe):** 0.94
  - Correctly identifies 94% of actual non-healthy loans.
- **F1 Score (f1):** 1.00
  - High harmonic mean of precision and recall.

#### Label 1 (High-Risk Loan):
- **Precision (pre):** 0.84
  - 84% of predicted high-risk loans are correct.
- **Recall (rec):** 0.94
  - Correctly identifies 94% of actual high-risk loans.
- **Specificity (spe):** 0.99
  - Correctly identifies 99% of actual non-high-risk loans.
- **F1 Score (f1):** 0.89
  - Harmonic mean of precision and recall for high-risk loans.

### Overall Model Performance:
- **Accuracy:** 99%

#### Weighted Average Metrics (avg / total):
- High precision, recall, and F1 score.

#### Confusion Matrix:
```
|                  | Predicted Healthy Loan (0) | Predicted High-Risk Loan (1) |
|------------------|----------------------------|-------------------------------|
| Actual Healthy Loan (0) | 18655                      | 110                               |
| Actual High-Risk Loan (1) | 36                           | 583                               |
```


### Logistic Regression Model Evaluation (OverSampled Data)

#### Label `0` (Healthy Loan):

- **Precision:** 1.00
  - Identifies all predicted healthy loans correctly.

- **Recall:** 0.99
  - Correctly identifies 99% of actual healthy loans.

- **F1-Score:** 1.00
  - High harmonic mean of precision and recall.

#### Label `1` (Non-Healthy Loan):

- **Precision:** 0.84
  - 84% of predicted non-healthy loans are correct.

- **Recall:** 0.99
  - Correctly identifies 99% of actual non-healthy loans.

- **F1-Score:** 0.91
  - Harmonic mean of precision and recall for non-healthy loans.

### Overall Model Performance:

- **Accuracy:** 99%
- **Macro Average Metrics:**
  - Precision: 0.92
  - Recall: 0.99
  - F1-Score: 0.95
- **Weighted Average Metrics:**
 - Precision: 0.99
  - Recall: 0.99
  - F1-Score: 0.99
#### Confusion Matrix:

|               | Predicted Healthy Loan (0) | Predicted Non-Healthy Loan (1) |
|---------------|---------------------------|--------------------------------|
| Actual Healthy Loan (0) | 18646                     | 119                            |
| Actual Non-Healthy Loan (1) | 4                         | 615                            |

### Summary
The overall accuracy of 99% in both models demonstrates strong performance in predicting both healthy and non-healthy loans, with a high precision, recall, and F1-scores for both classes.
The F1-Score for predicting non-healthy loans increased from 0.89 to 0.91 with oversampling, hence suggesting for better balance in predicting non-healthy loans the oversampled model may be preferred.
 

