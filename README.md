# Loan Prediction

This dataset comes from the Kaggle competition, hosted [here](https://www.kaggle.com/c/loan-default-prediction/). The description and the evaluation used will be presented.

## Description

This competition asks you to determine whether a loan will default, as well as the loss incurred if it does default. Unlike traditional finance-based approaches to this problem, where one distinguishes between good or bad counterparties in a binary way, we seek to anticipate and incorporate both the default and the severity of the losses that result. In doing so, we are building a bridge between traditional banking, where we are looking at reducing the consumption of economic capital, to an asset-management perspective, where we optimize on the risk to the financial investor.

This competition is sponsored by researchers at Imperial College London.

## Evaluation

This competition is evaluated on the mean absolute error (MAE): 

<img src="https://render.githubusercontent.com/render/math?math=\textrm{MAE} = \frac{1}{n} \sum_{i=1}^n | y_i - \hat{y}_i|">

where

* n is the number of rows
* $\yhat_i$ is the predicted loss
* $y_i$ is the actual loss

## Data Introduction

This data corresponds to a set of financial transactions associated with individuals. The data has been standardized, de-trended, and anonymized. You are provided with over two hundred thousand observations and nearly 800 features.  Each observation is independent from the previous. 

For each observation, it was recorded whether a default was triggered. In case of a default, the loss was measured. This quantity lies between 0 and 100. It has been normalised, considering that the notional of each transaction at inception is 100. For example, a loss of 60 means that only 40 is reimbursed. If the loan did not default, the loss was 0. You are asked to predict the losses for each observation in the test set.

Missing feature values have been kept as is, so that the competing teams can really use the maximum data available, implementing a strategy to fill the gaps if desired. Note that some variables may be categorical (e.g. f776 and f777).

The competition sponsor has worked to remove time-dimensionality from the data. However, the observations are still listed in order from old to new in the training set. In the test set they are in random order.
