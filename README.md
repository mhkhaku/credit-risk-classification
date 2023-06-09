# credit-risk-classification

## Overview of the Analysis
- Lenders operate on the fundamental assumption that the borrowers they lend money or assets to will repay their debts. However, there is always a risk associated with lending, as some borrowers may default on their loans or fail to return the assets, leading to financial losses for the lenders. To mitigate this risk, lenders use various techniques to assess the creditworthiness of borrowers. In this analysis, we will use Machine Learning to examine a dataset of a peer-to-peer lending service company's past lending activities to construct a model that can identify the probability of borrowers defaulting on their loans.

- In this analysis, the variable of interest is y_prediction, which represents the predicted outcome. Initially, I extract data from the loan_status column and store it as the y_variable. Using the value_counts method, I determine the count of good and bad loans present in the dataset. This information is further used to construct test data for training and prediction purposes.

- My aim is to distinguish between low-risk (healthy) and high-risk (non-healthy) loans by utilizing a machine learning model. For this purpose, I have developed two models using LogisticRegression and resampling techniques. The Logistic Regression Algorithm is particularly well-suited for this task as it is commonly used to calculate the probability of a target variable in classification problems.

## Results

- Machine Learning Model 1 (LogisticRegression):

  - balanced_accuracy_score = 0.9520479254722232
  - precision 0=1.00, 1=0.85
  - recall 0=0.99, 1=0.91

- Machine Learning Model 2 (RandomOverSampler):

  - balanced_accuracy_score = 0.9936781215845847
  - precision 0=0.99, 1=0.99
  - recall 0=0.99, 1=0.99

## Summary

After conducting my analysis, I have concluded that the RandomOverSampler model is the most effective in identifying individuals who may be at a higher risk of defaulting on loans due to their credit history. The Logistic Regression model that was trained with OverSampled data demonstrated superior performance compared to the model that was trained with Imbalanced data, primarily due to the balanced nature of the dataset. As a result, the model achieved a higher accuracy score and recall rate, indicating its capability to make fewer errors when classifying non-healthy loans. In light of these findings, I would recommend using the RandomOverSampler model due to its higher accuracy and ability to identify classification errors.
