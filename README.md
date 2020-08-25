# Project Overview

In today’s increasingly electronic society, Credit Card transactions has come to be the
primary way many people pay for purchases and there is evidence that using credit card
frequently may lead to frauds. The figures are expected to grow rapidly each year.

 According to the figures, there is increase of 45% in credit card frauds in the year 2016-2017
and in the year 2017-2018 it increased to 48%.

When banks lose money because of credit card fraud, cardholders pay for all of that loss
through higher interest rates, higher fees, and reduced benefits. Hence, it is in both the banks
and the cardholder’s interest to reduce illegitimate use of credit cards by early fraud
detection.

Credit Card companies are approaching data scientists in order find a solution to this problem.
To solve this problem, model can be build which flags the fraud transactions and gives an
alert to the companies and the cardholders. This model can be designed using both
supervised learning (requires labelled data to train the algorithm) and unsupervised learning
(requires unlabelled data and can tag the outlier transactions as fraud) methods.

I implemented three different machine learning models in order to classify, to the highest
possible degree of accuracy, credit card fraud from a dataset.

After initial data exploration, I trained and tested logistic regression model, a k-means
clustering model, and Random Forest classifier model to detect the fraudulent transanctions
and identified the best capable model.

A research collaboration of Worldline and the Machine Learning Group of ULB on big data
mining and fraud detection have worked on the datasets provided by Kaggle in order to find
a better model to tag the fraud credit card transactions


# Problem Statement

The goal of this project is to find out whether a cardholder transaction is fraud or not. In
supervised learning, the Random forest classifier model gives information about a
transaction and assigns 1if the transaction is fraud and 0 if the transaction is good.

In unsupervised learning, the K-Means clustering model is used in which the transactions
which lie farther away (outliers) from the normal transactions are considered as fraud
transactions. The model performance is evaluated using recall score rather than accuracy
score.

# Metrics

The distribution of the data was visualised and the features transformed using logarithmic
transformations. The features are then standardized in order to achieve zero mean and equal 
variance. I built models using supervised and unsupervised learning method, and compared
their performance results.

For supervised model, , the dataset with label feature is fitted to a supervised classifier and the
area under the Precision-Recall Curve and Recall Score is calculated and the predicted results
are then compared with the actual results

For unsupervised model, the dataset without the label feature is fitted to unsupervised
algorithm, and the outliers are tagged as fraud transactions, and compared with the actual label
to evaluate the performance of the model.

The precision-recall curve shows the trade-off between precision and recall for different
threshold. A high area under the curve represents high recall and high precision, where high
precision relates to a low false positive rate, and high recall relates to a low false negative rate.

For our problem statement, the model have precision -recall curve and recall score nearly
equal to 1.The reason to consider area under precision-recall as a performance metric for both
the supervised and unsupervised models is to capture the fraudulent transactions, which are
false negatives in the prediction results. Therefore, the less the number of false negatives, the
better the model captures the fraudulent transactions. The area under precision-recall is equal
to 1, if the number of false negatives is zero. Recall Score is the ratio of True Positives and
Sum of True Positives and False Negatives.

# Data Exploration

For this project, the datasets which contains transactions made by credit cards by European
cardholder available on Kaggle is used.

This dataset presents transactions that occurred in two days, where we have 492 frauds out of
284,807 transactions. The dataset contains only numerical input variables which are the result
of a PCA transformation. It consists 28 Principal Components, along with Time and Amount
of the Transaction.

Features V1, V2, ... V28 are the principal components obtained with PCA, the only features
which have not been transformed with PCA are 'Time' and 'Amount'.

Feature 'Time' contains the seconds between each transaction and the first transaction in the
dataset.
 The feature 'Amount' is the transaction Amount.
 Feature 'Class' is the response variable and it takes value 1 in case of fraud and 0 otherwise.
 For the feature distribution, Amount feature was used because most of the other features are
 principal components and wouldn’t give much information about the real features. 
