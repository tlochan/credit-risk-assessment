# credit-risk-assessment
Supervised Machine Learning to Assess Credit Risk

## Overview of the Analysis

The purpose of this analysis was to leverage Supervised Machine Learning to determine whether a potential borrower would be a reliable investment based on their prior financial data. Using historical data of healthy and risky loans we investigated the borrowers based on their credit history (income, debt, number of banking accounts, & delinquent payments) and the qualities of the loan itself (total amount & interest rate). Predicting whether a loan would be healthy or risky helps financial institutions to minimize losses and lend confidently. 

I applied a Logistic Regression model to the dataset after it was split into training and testing sets. The model uses all of the loan and borrower data to classify whether a loan will be healthy or default before the end of its term. By fitting the model to 75% of the data and then testing it out on the remaining borrowers, we can determine how reliable the model would be on future clients. 
## Results
* Machine Learning - Logistic Regression:
    * Accuracy: 99% Overall
    * Precision: 
        * ~100% for healthy loans
        * 85% for risky loans
    * Recall: 
        * 99% for healthy loans
        * 91% for risky loans

## Summary

The logistic regression model does an exceptional job at predicting the 0/healthy loans with a precision and recall of 100% and 99%. The confusion matrix shows that the model predicted 18663 health loans correctly with 102 false negatives and 56 false positives. Relative to the total amount of data points, it rarely misses out on the reliable borrowers. 

The model does a worse job predicting the 1/high-risk loans with a precision and recall of 85% and 88% respectively. Relative to the 563 correctly predicted risky loans, the 102 false negatives vs 56 false positives indicate the model over-predicts risky loans. 

From the perspective of loan-provider, it is better to tune the model this way to avoid losses on edge cases. Few of the loans predicted to be healthy end up defaulting. In other words, this model is useful for preliminary credit applications as it will reliably predict creditworthy borrowers.

