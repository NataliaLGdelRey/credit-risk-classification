# Module 12 Report Template

## Overview of the Analysis

-------------------------------------------

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
* Explain what financial information the data was on, and what you needed to predict.
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
* Describe the stages of the machine learning process you went through as part of this analysis.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).

- The purpose of the analysis is to predict whether a loan is healthy or high-risk based on various financial data.
- The financial data includes loan size, interest rate, borrower income, debt to income, number of accounts, derogatory marks, total debt and loan status.
- The analysis involves building a machine learning model and analyze its performance for predicting healthy loans and high-risk loans.

- The data contains 77,536 observations with 8 columns, including a target column called loan_status.
- The loan_status column has two classes (target values): 0 for healthy loans and 1 for high-risk loans.
- The value counts for the target variable (target values - value_counts) are 0: 75036 and 1: 2500.

- The stages of the machine learning process are as follows:
  - Data pre-processing and cleaning.
  - Splitting the data into training and testing sets.
  - Building and training a Logistic Regression model on the original imbalanced data.
  - Evaluating the model's performance and analyzing its results.

- Logistic Regression model is used in this analysis.

## Results

-----------------------------------------------

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1: Logistic Regression
  * Description of Model 1 Accuracy, Precision, and Recall scores.

  accuracy (macro avg): precision = 0.94, recall = 0.94, f1-score = 0.94
  accuracy (weighted avg): precision = 0.99, recall = 0.99, f1-score = 0.99

    -	Healthy Loans (0): precision = 1.00, recall = 1.00, f1-score = 1.00
    -	High-Risk Loans (1): precision = 0.87, recall = 0.89, f1-score = 0.88


* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.

## Summary

-------------------------------------------------

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.


- Logistic regression model successfully predicts healthy loans but it does it worse when identifying high-risk loans.

- Outcome summary:
-----------------------
  - Healthy loans (0): precision = 1.00, recall = 1.00, f1-score = 1.00
  - High-risk loans (1): precision = 0.87, recall = 0.89, f1-score = 0.88

- The accuracy (macro avg) score was 0.94. The main accuracy was 0.99.

The logistic regression model performed well in predicting healthy loans. Therefore, I recommend using the logistic regression model on the data for predicting healthy loans. However when predicting high-risk loans, although it had a precison of 0.87, it might be a good thing to consider training another model to perform better in predicting high-risk loans. However, the choice of model may depend on the specific problem and business requirements of the user, and it is essential to consider the consequences of making errors in the prediction of both healthy and high-risk loans. This model could be used if it is more important to predict the 0 or the 1. It could be used to check that a loan is healthy and safe and use some other model to chek the high-risk loans.
