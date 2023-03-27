# Credit-Risk-Classification Analysis Report

## Overview of the Analysis

The purpose for creating this machine learning model is to evaluate the creditworthiness of borrowers.

To begin with, some of the financial information used were loan size, interest rate, borrower income, debt to income, number of accounts, derogatory marks, total debt, and loan status. The labels set were retrieved from the loan status information or column in the dataframe, and the featrues were all of the other financial information provided. The value_counts() counts the amount of 0's and 1's. The 0's signify a healthy loan and 1's signify a high-risk loan. I then split the data into two data sets with train_test_split.

Next,  I created two Logistic Regression Models with the training data. In the first model, I used the original data and then fit the model with the training data. Then I made the predictions using the testing data. Lastly, I looked at the balanced_accuracy_score and the accuracy_score to see what the difference was between the average per class sample and total samples (this was mostly to further my analysis a little further in order to aid my understanding). I generated a confusion matrix, and printed the classification report as well. The same steps were done for the second model; however, resampled trained data was used. The data was resampled using RandomOverSampler. When oversampling the data, you can see that the 1's and 0's are now balanced at 75,036. Before oversampling, the amount of 0's was 75,036 and 1's was 2,500.

## Results

* Machine Learning 1:

  * Balanced accuracy score is .95
  * Precision: for 0's is 1.00; for 1's is .85
  * Recall: for 0's is .99; for 1's is .91
* Machine Learning 2:

  * Balanced accuracy score is .99
  * Precision: for 0's is .99; for 1's is 1.00
  * Recall: for 0's is 1.00; for 1's is .99

## Summary

Based on the results, the second model seems to perform best. Oversampling the data, thus balancing the data, helped get a better picture of the healthy and high-risk loans. For this particular instance, it would be more important to predict the 1's which are the high-risk loans. With one bad loan, you can outweigh the profit of good loans. In other words, the cost of a bad loan would be greater than losing out on a good loan.
