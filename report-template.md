# Project Title
Module-20-Supervised-Learning

## Overview of the Analysis
In this analysis, we try to use machine learning to determine the risk associated with new loan applications. Using historical lending peer to peer data to determine how risky a loan application will be.  <br>

For the features of this analysis, we had: <br>
* Loan Size
* Interest Rate
* Borrower Income
* Debt Income
* Number of Accounts
* Derogatory Marks
* Total Debt <br>

First, the data is imported into a dataframe, allowing for efficient data manipulation and analysis. The labels and features variables are then created by separating the dataset into dependent and independent variables for prediction. A train-test split is performed to divide the data into training and testing sets.<br>
Next, a logistic regression model is created using the original data. This algorithm is suitable for binary classification tasks. The model is trained using the training set, adjusting its parameters to minimize the difference between predicted and actual labels. The trained model is then used to make predictions on the testing set, and the predicted labels are saved for later evaluation.
<br>
The performance of the logistic regression model is assessed using various metrics:accuracy score, confusion matrix, and classification report. The training data can be resampled using the RandomOverSampler module from the imbalanced-learn library. The entire process, from model creation to evaluation, is repeated using the resampled training data.

## Results
* Machine Learning Model 1:
  * Accuracy: macro avg: 95%, weighted avg: 99%; Accuracy is very high for this   model, especially when considering the number of data for each class. 
  * Precision: 0: 99%, 1: 91%; Precision for this model is high for both 0 and 1.
  * Recall: 0: 100%, 1: 85%; Recall for this model is 100% correct when predicting 0 and 85% correct when predicting 1.

* Machine Learning Model 2:
  * Accuracy: macro avg: 99%, weighted avg: 99%; Accuracy is very high for this   model. 
  * Precision: 0: 99%, 1: 99%; Precision for this model is high for both 0 and 1.
  * Recall: 0: 100%, 1: 84%; Recall for this model is 100% correct when predicting 0 and 85% correct when predicting 1.

## Summary
Based on the evaluation metrics, the model with the oversampling technique emerges as the best performer among the machine learning models. This conclusion is supported by metrics such as accuracy score, confusion matrix, and classification report. By addressing class imbalance, the oversampling model demonstrates improved accuracy in predicting both healthy and risky loan applications.<br>

Considering the problem at hand, accurately predicting both classes is crucial. Misclassifying a healthy application as risky could lead to granting a problematic loan, while misclassifying a risky application as healthy might result in rejecting a potentially viable one. Therefore, it is vital to achieve high accuracy in predicting both 0 and 1 classes. With its superior accuracy and ability to handle class imbalance, the oversampling model is recommended for this task, as it shows promising performance in accurately identifying both healthy and risky loan applications.

