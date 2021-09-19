# Bank-Personal-Loan-Modelling

## Overview
This project is about a bank which has a growing customer base where the majority of customers are depositors with varying size of deposits. Apart from the majority of customers that are depositors, several customers are also borrowers (asset customers). The bank planned to expand the asset customers to earn more through the interest on personal loans 
by converting the depositors (potential customers) to personal loan customers while retaining them as depositors. A campaign that the bank ran last year for potential customers showed a healthy conversion rate of over 9% success. This has encouraged the retail marketing department to devise campaigns for better target marketing that will increase the 
success ratio while at the same time reduce the cost of the campaign by using a model that will help them identify the potential customers who have a higher probability of purchasing the loan.

## Tools Used
- Python version: 3.6.9
- Packages: Numpy, Matplotlib, pandas, jcopml, scikit-learn

## Data Cleaning
After loaded the data, I needed to clean it up so that it was usable for the machine learning model. There are several values on the experiences feature that below 0, so I replace these values with 0 (these values also can be imputed with mean or median). 

## Exploratory Data Analysis
Based on the exploratory data analysis results, it is shown that the target label data (Personal_Loan) is imbalanced, so it needs weighting and scored by f1 score metrics. I also plotted three features among several other features that influenced the customer's decision education level, income, and credit card spending cost average per month that are shown below. 

<img src="https://github.com/azizamir/bank-personal-modeling/blob/main/results/binned%20income_loan.png" width="500" height="300" /> <img src="https://github.com/azizamir/bank-personal-modeling/blob/main/results/education_loan.png" width="300" height="300" /> 
<img src="https://github.com/azizamir/bank-personal-modeling/blob/main/results/ccavg-income_loan.png" width="400" height="300" /> <img src="https://github.com/azizamir/bank-personal-modeling/blob/main/results/target.png" width="300" height="300" /> 

## Model Building
After done with dataset splitting (train-test ratio = 80:20) and preprocessing (encode the categorical features), I started build the machine learning model using three algorithms
- Logistic Regression = used as the baseline model due to its simplicity and capability to handle an imbalanced dataset
- Random Forest Classifier = used due to its characteristics (prone overfit algorithm, low bias, high variance) so it will fit for handling a dataset that having a large number of data points and relatively small amount of features
- XGBoost Classfier = used due to its characteristics (prone overfit algorithm, low bias, high variance, tree-based) so it will fit for handling a dataset that having a large number of data points and relatively small amount of features

## Model performance 
The random forest classifier model shown a very well performance compared with other models. The result scored by f1 metrics due to imbalanced data.
- Logistic Regression f1 score = 0.78
- Random Forest Classifier f1 score = 0.94
- XGBoost Classfier f1 score = 0.92
