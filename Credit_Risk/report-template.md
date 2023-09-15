# Module 12 Report Template

## Overview of the Analysis

We conducted a retrospective analysis of a dataset of n = 77,536 banking records to determine if our classifiers could predict the credit worthiness of bank clients. We deployed a logistic regression model using the scikit-learn linear_model library. Covariates included in the model were loan_size, interest_rate, borrower_income, debt_to_income, num_of_accounts, derogatory_marks, and total_debt. No interaction effects were examined. The outcome variable, loan_status, was heavily biased, with 75,036 records being healthy loans and only 2,500 records having a high-risk label. This was only partially mitigated in the process of splitting our data using train_test_split from the scikit-learn moel_selection library into a training and a testing set. We therefore resampled the training data using RandomOverSampler from the imbalanced-learn over_sampling library. We then fit the regression model to our resampled training data and used the parameterized model to predict outcomes using inputs from the testing data and comparing against the actual outcomes. 


## Results


* Machine Learning Model 1:
  * Model 1 Accuracy: 0.95
  * Precision
    * Healthy loan: 1.00
    * High-risk loan: 0.85
  * Recall
    * Healthy loan: 0.99
    * High-risk loan: 0.91



* Machine Learning Model 2:
  * Model 2 Accuracy: 0.99
  * Precision
    * Healthy loan: 1.00
    * High-risk loan: 0.84
  * Recall
    * Healthy loan: 0.99
    * High-risk loan: 0.99

## Summary

Both models performed well, and with oversampling (Model 2) performed best. There was an increase in performance on recall for High-risk loans with only a small decline in precision. Given the minute difference in precision and the large gain in recall I would recommend Model 2. 
