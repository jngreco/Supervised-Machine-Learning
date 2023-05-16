# Module 12 Report

## Overview of the Analysis

* This analysis was conducted in order to create a model that can be used to identify the creditworthiness of borrorowers. 
* Data used in this analysis includes a CSV with over 77,000 rows of data. The CSV contains the following information:   
   1. loan_size
   2. interest_rate
   3. borrower_income
   4. debt_to_income
   5. num_of_accounts
   6. derogatory_marks
   7. total_debt
   8. loan_status
* A logistic model was fit using training data `X_train` and `y_train`.
* Model's performance was evaluated based on the following: 
   * calculated accuracy score 
   * confusion matrix 
   * classification report

## Results
### Machine Learning Model 1:
* Balanced Accuracy Score: 0.952047 (95%) 
* Precision `0` (healthy loan): 85% 
* Precision `1` (high-risk loan): 100% 
* Out of the `18,765` loans with a status of **healthy**, the model predicted `18,663` correctly and `102` incorrectly 
* Out of the `619` loans with a status of **unhealhty** (high-risk), the model predicted `563` as correctly and `56` incorrectly

Based on the balanced accuracy score of approximately 0.95 (95%), our confusion matrix, and the results of our classification report, our model appears to perform very well. However, it is important to note that over half of the available entries in the dataset are categorized as healthy/low-risk loans. This discrepancy is reflected in our classification model, which shows us that the model predicted healthy loans 100% of the time, and non-healthy loans only 85% of the time. **In other words, the model is better able to preduct healthy loans than non-healthy loans.**  


### Machine Learning Model 2:
* Balanced Accuracy Score: 0.993678 (99%) 
* Precision `0` (healthy loan): 84% 
* Precision `1` (high-risk loan): 100% 
* Out of the `18,765` loans with a status of **healthy**, the model predicted `18,663` correctly and `116` incorrectly 
* Out of the `619` loans with a status of **unhealhty** (high-risk), the model predicted `615` correctly and `4` incorrectly

The model performs more accurately with the ROS data compared to the model with original data. The accuracy score has increased to .99 (99%) with the oversampled data, compared to .95 (95%) accuracy score with the original data. 

## Summary

**Of the two models, model 2 functions with a higher BAC (99%)**

In terms of overall risk for the company, model 2 is a safer option for a company looking to use machine learning to predict the creditworthiness of loan applicants. If a healthy loan is mistakenly categorized as risky, the financial loss is minimal compared to a risky loan being categorized as healthy. An appeal process could be implemented to mitigate the already slim chance of a healthy loan being falsley flagged as risky. 

