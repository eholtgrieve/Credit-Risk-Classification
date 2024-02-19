# Credit-Risk-Classification

# Instructions
The instructions for this Challenge are divided into the following subsections:
  - Split the Data into Training and Testing Sets
  - Create a Logistic Regression Model with the Original Data
  - Write a Credit Risk Analysis Report

# Split the Data into Training and Testing Sets
Open the starter code notebook and use it to complete the following steps:
 - Read the lending_data.csv data from the Resources folder into a Pandas DataFrame.
  - Create the labels set (y) from the “loan_status” column, and then create the features (X) DataFrame from the remaining columns.
    - NOTE: A value of 0 in the “loan_status” column means that the loan is healthy. A value of 1 means that the loan has a high risk of defaulting.
  - Split the data into training and testing datasets by using train_test_split.

# Create a Logistic Regression Model with the Original Data
Use your knowledge of logistic regression to complete the following steps:
  - Fit a logistic regression model by using the training data (X_train and y_train).
  - Save the predictions for the testing data labels by using the testing feature data (X_test) and the fitted model.
Evaluate the model’s performance by doing the following:
- Generate a confusion matrix.
- Print the classification report.
- Answer the following question:
    - How well does the logistic regression model predict both the 0 (healthy loan) and 1 (high-risk loan) labels?
 
# Analysis
The purpose of this analysis was to create and train a model to predict loan risk of borrowers using data from a lending services company. The target financial information was the "loan_status" variable, which determined whether or not a borrower was at a high risk of defaulting on their loan. The features of the financial information which were factors used in determining eligibilty were things like loan size, interest rate on the loan, the borrower's income, and the borrower's total debt. 
The process of the machine learning was as follows:
  - Read in the csv data into a data frame
  - Separate the target data from the features into the y and X variables respectively
  - Split the data into training and testing datasets using the "train_test_split" function
  - Create a logistic regression model using the original data
  - Fitting the model using the training dataset
  - Make predictions using the testing feature data and the fitted model
  - Evaluating the model's performance based on its accuracy score, confusion matrix, and classification report
The only method used in this analysis was the Logistic Regression on our one model that I then fitted to the original data. 
  
# Results
              precision    recall  f1-score   support

           0       1.00      0.99      1.00     18765
           1       0.85      0.91      0.88       619

    accuracy                            0.99     19384
    macro avg       0.92      0.95      0.94     19384
    weighted avg    0.99      0.99      0.99     19384

# Summary
The model did a good job in predicting both healthy and high-risk loans, with an accuracy score of 99.18%. 
The precision score of 100% and 85% for healthy versus high-risk loans respectively tells us that, while healthy loans were classified correctly 100% of the time, high-risk loans were classified correctly only 85% of the time.
With a recall score for healthy loans at 99% and high-risk loans at 91%, this implies that loans that were actually healthy were classified correctly 99% of the time and loans that were actually high-risk were only classified correctly 91% of the time. 

With these results, I wouldn't recommend using this model since it's only being able to correctly predict 85% of high-risk loans. It's important to correctly identify whether or not a borrower will fully be able to pay back loans 
or else the company could easily lose out on money and having a precision number that low would make it easy to approve the wrong borrowers.