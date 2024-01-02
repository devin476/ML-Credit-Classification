# Module 12 Report Template

## Overview of the Analysis

## Purpose of the Analysis

The primary objective of this analysis is to develop a machine learning model capable of predicting the likelihood of loan default. By accurately identifying high-risk loans, financial institutions can make more informed lending decisions, thereby mitigating potential financial losses.

## Financial Data Overview

The analysis was conducted on a dataset comprising various financial attributes related to personal loans. Key variables included:

- Loan Amount
- Term of Loan
- Credit Score
- Annual Income
- Debt to Income Ratio
- Past Default History

The target variable for prediction was the loan status, categorized as 'Healthy' (low-risk) or 'High-Risk'.

## Methods and Models Used

- **Logistic Regression**: Chosen for its effectiveness in binary classification problems. It served as the primary model to predict the probability of a loan being high-risk.
- **Resampling Techniques**: Due to the imbalance in the dataset, resampling methods like `RandomOverSampler` were employed to create a more balanced distribution of the target classes.

## Results

## Model 1: Logistic Regression Analysis

The logistic regression model demonstrates proficient capability in predicting labels for both healthy and high-risk loan categories. However, the model's performance exhibits variation across these categories.

- **Precision**: 
  - Healthy Loans: 100%
  - High-Risk Loans: 85%
- **Recall**: 
  - Healthy Loans: 99%
  - High-Risk Loans: 91%

The variation in model performance can be attributed to the data distribution, where the model has been exposed to a significantly larger number of healthy loans (over 18,000 instances) compared to high-risk loans (619 instances). The model's accuracy in label recognition and recall is influenced by the frequency of exposure to each label.

## Model 2: Impact of Oversampling on Logistic Regression

Comparing the original logistic regression model with a version utilizing oversampled data reveals key differences:

- **Precision Rates**: Relatively consistent with the original model.
- **Recall Rate for High-Risk Loans**: Improved substantially from approximately 91% to about 99%.

This improvement is also observed in the recall rates for healthy loans.

## Summary

In conclusion, the application of oversampled data in the logistic regression model markedly enhances its effectiveness in predicting high-risk loans:

- **Recall Rate for High-Risk Loans**: Increased from 91% to 99%.
- **Precision Rate for High-Risk Loans**: Increased from 85% to 99%.

It is important to note, however, that the model's exposure to healthy loans far exceeds that of high-risk loans. This disparity in exposure levels is a crucial factor in the model's overall ability to accurately identify and recall each label.