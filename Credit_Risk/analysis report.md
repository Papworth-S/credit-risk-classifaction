# Module 20 Report 

## Overview of the Analysis

For this assignment we used a popular machine learning model called the Logistic Regression Model.  We provided it some data to see if we can have the model predict creditworthiness of future borrowers:

* The purpose of the analysis was to see if based on the data provided can we get a prediction withing an acceptable percentage.
* We provide the model with seven columns as the features (`loan_size`,`interest_rate`,`borrower_income`,`debt_to_income`,`num_of_accouts`,`derogatory_marks`)
* The label we removed was `loan_status`, since this was going to be the variable we are wanting the model to predict.  This is either a `0` or a `1`.  `0` is a healthy loan and `1` is at “high risk”  of defaulting.
* For this model we went with the default split of training and testing data.  75% went towards training, and the remaining 25% was used for testing the model.
* We look at the results sing both a confusion matrix and classification report which will be explained below.

## Results

* Machine Learning Model 1 (we only used one model with this data:
  * First, we use a confusion matrix to get a quick overview of the models overall accuracy.  We see that majority of positive predictions where actual predictions. And we also see that most of the predicted negatives where actual negatives.  We also see that there were more false negatives than false positives and that might not be the best result for this model.  So we took it one step further and looked a  classification report 
  * The classification report show us a couple of things
	* Precision for healthy loans is 100% but for high risk loans is only 85%.
	* Recall is above 90% for both
	* The F-1 score is 100% for healthy but only 88% for high risk
	* The overall accuracy for this model is 99% but favors predictions of healthy loans

## Summary

In Summarize:
The logistic regression model does an excellent job predicting the `0` healthy loan with a precision of 1.00 or "perfect" 100% and a recall of .99 or 99%.  This makes it an excellent model for predicting future health loans.  Now for the `1` high-risk loans, it is not quite as good (but this has a bit to do with the size of the `1` in the dataset; there are only 619 records out of ~20k).  The precision is .85, so there could be about 15% of the loan being called high-risk are not high-risk.  With a recall of .91, there is pretty good confidence that those labeled high risk are high risk.  Overall, this model gets a .99, so it is a model that can be used again with confidence.
