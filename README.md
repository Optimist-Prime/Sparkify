## Overview
**Sparkify** is a fictitious digital streaming service by Udacity.  

Here, our job is deep mining the customers' data and implement appropriate model to predict customer churn as follow steps:
- Clean data: fill the nan values , correct the data types, drop the outliers.
- EDA: exploratory data to look features' distributions and correlation with key label (churn).
- Feature engineering: extract and found customer-features and customer-behavior-features; Implement standscaler on numerical features.
- Train and measure models:  I choose logistic regression, linear svm classifier, decision tree and random forest classifier to train a baseline model and tuning a better model from best of them. It is worth mentioning that this data is unbalanced because of less churn customers, so we choose `f1 score`  as a metrics to measure models' performance.

## Installation

- Python 3.6
- PySpark ML
- Jupyter

## Results

The baseline of four machine learning methods: Logistic Regression, Linear SVC, Decision Tree Classifier and Random Forest Classifier. 

Though the `LinearSVC` spent more training time, but it can get the highest f1 score 0.702. And the `LogisticRegression` has a medium training time and f1 score, maybe I can tuning it to get a higher 
score. So I'll choose `LinearSVC` and `LogisticRegression` to tuning, and the result is as follows:

| Model Name         |  F1-score  | Training Time(s) |
| ------------------ | ---------- | ---------------- |
| LogisticRegression | 0.099071   | 14.5863          |
| LinearSVC          | 0.7045     | 60.1778          |

Considering this is only a quit mini dataset and our purpose is scaling this up to the total 12G  dataset, so, the logistic regression is the best model from now on in this project.

Please check my blog post to get more details, here is the [link](https://mohit-gupta.medium.com/churn-or-not-in-sparkify-2a473320c40d).

## References

Dataset provided by [Udacity](https://www.udacity.com/).
