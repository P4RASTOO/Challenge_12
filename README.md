

<img width="578" alt="Screenshot 2023-08-05 at 6 22 01 PM" src="https://github.com/P4RASTOO/Challenge_12/assets/132952512/b6a47815-ff15-44e7-b45f-74aed3feca13">


# Challenge_12 Report
## Overview of the Analysis
The purpose of the analysis was to build a machine learning model to predict loan statuses (healthy loans vs. high-risk loans) based on financial information. The goal was to develop a predictive model that could assist in identifying loans that might be at a higher risk of defaulting. The data used in the analysis contained various financial attributes related to loans, such as loan amount, interest rate, credit score, debt-to-income ratio, employment status, and other relevant features. The target variable for prediction was the "loan_status," which contained binary values (0 and 1) representing whether the loan was re-paid or defaulted.

The stages of the Machine Learning Process used include; 
1) Data loading and exploration: Load the dataset and explore its structure, statistics, missing values, and data types. 
2) Data preprocessing: Handle missing values, encode categorical variables, and scale numerical features if needed. 
3) Data splitting: Divide the dataset into training and testing sets for model evaluation. 
4) Model selection and training: Select the appropriate algorithm (eg; Logistic Regression) and train the model on the training data. 
5) Model evaluation: Assess the model's performance on the testing data using metrics like accuracy, precision, recall, and F1-score. 
6) Resampling (Oversampling): Use techniques like RandomOverSampler to balance classes and improve model performance on imbalanced datasets. 

Methods Used;
1) Logistic Regression that is a classification algorithm for binary classification problems. It models the relationship between the dependent variable (loan status) and independent variables (financial attributes) using the logistic function. 
2) RandomOverSampler that is a resampling technique used to balance imbalanced datasets by creating synthetic samples for the minority class (eg; high-risk loans) to match the majority class (eg; healthy loans).

## Results

Description of the balanced accuracy scores and the precision and recall scores of all machine learning models;
* Machine Learning Model 1:
Description of Model 1 Accuracy, Precision, and Recall scores:
For the label 0 (Repaid/Healthy Loan):
Precision: 1.00
Recall: 1.00

F1-score: 1.00
For the label 1 (Defaulted/High-Risk Loan):
Precision: 0.86
Recall: 0.91
F1-score: 0.88
With an accuracy of 0.99 and high precision, recall, and f1-score values for both labels, the logistic regression model seems to be highly effective in predicting both 0 (healthy loan) and 1 (high-risk loan) labels in the dataset.


* Machine Learning Model 2:
Description of Model 2 Accuracy, Precision, and Recall scores:
For the label 0 (Healthy Loan):
Precision: 1.00
Recall: 0.99
F1-score: 1.00
Support: 15001

For the label 1 (High-Risk Loan):
Precision: 0.85
Recall: 0.99
F1-score: 0.92
Support: 507
The high precision and recall values for both labels indicate that the model is effective in predicting both classes. The F1-scores, which are harmonic means of precision and recall, further validate the model's balance in handling both classes. Additionally, the high accuracy of 0.99 further supports the model's overall effectiveness in classifying loans into healthy and high-risk categories.

## Summary
Summary of the Results of Machine Learning Models:

* Logistic Regression Model with Original Data:
Precision (Label 0): 1.00
Recall (Label 0): 0.99
F1-score (Label 0): 1.00
Precision (Label 1): 0.85
Recall (Label 1): 0.99
F1-score (Label 1): 0.92
Accuracy: 0.99
Balanced Accuracy Score: 0.96
* Logistic Regression Model with Resampled Data:
Precision (Label 0): 1.00
Recall (Label 0): 0.99
F1-score (Label 0): 1.00
Precision (Label 1): 0.85
Recall (Label 1): 0.99
F1-score (Label 1): 0.92
Accuracy: 0.99
Balanced Accuracy Score: 0.96

Both logistic regression models (with original and resampled data) performed similarly in terms of precision, recall, F1-score, accuracy, and balanced accuracy score. For both models, the precision for predicting label 0 (healthy loan) was perfect (1.00), and the recall for predicting label 1 (high-risk loan) was high (around 0.99). The F1-scores for predicting label 1 were 0.92 in both cases, indicating a good balance between precision and recall.

Based on the evaluation metrics and performance, it seems that the logistic regression model with original data and the one with resampled data perform equally well for predicting loan statuses. Since both models yield similar results, it may be more practical to use the logistic regression model with original data, as it requires less preprocessing (no need for resampling). Additionally, using the original is computationally more efficient.

However, the choice of the model might depend on the specific problem and the business requirements. For example, if correctly predicting high-risk loans (label 1) is of utmost importance to minimize financial risks, then a slight preference may be given to the model with resampled data, as it achieved marginally better recall for label 1. Conversely, if overall accuracy and efficiency are the primary concerns, the logistic regression model with original data would be a reasonable choice.
