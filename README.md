# Credit Risk Defaults comparative study

## Introduction

This project conducts a comparative study of different machine‑learning and deep learning models, evaluating both their classification accuracy and their ability to estimate the true probability of an individual’s class membership. Classification performance is assessed using metrics such as error rate, while probability calibration is evaluated via the Sorting Smoothing Method in a risk‑management context. The analysis using the “Default of Credit Card Clients, Taiwan 2005” dataset from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/350/default+of+credit+card+clients?fbclid=IwY2xjawJO-XdleHRuA2FlbQIxMAABHVTywu6Qx2uUPBRIr4Ok_TK7dswnh-qnUJn0xb0ArjPZ7-UTknqTCHVcJg_aem_4Yv9f48SV0XG_RLQOy5qxQ).

## Credit Card Default
Credit card default occurs when a cardholder fails to make at least the minimum payment by the due date, prompting issuers to impose penalties, reduce credit limits, or close the account. Defaults often stem from extending credit without fully assessing an applicant’s ability to repay, which can lead to overspending and unmanageable debt. In credit risk assessment, lenders focus on the **probability of default (PD)**, and this project aims assess the performance of different model to accurately predic PD to support better risk management and lending decisions.

## Data Overview

The study took payment data in October, 2005, from an
important bank (a cash and credit card issuer) in Taiwan
and the targets were credit card holders of the bank.
Among the total 30,000 observations, 6636 observations
(22.12%) are the cardholders with default payment. This
research employed a binary variable – default payment
(Yes = 1, No = 0), as the response variable. 

There are 23 explanatory variables:

This research employed a binary variable, default payment (Yes = 1, No = 0), as the response variable. \
This study used the following 23 variables as explanatory variables:
- LIMIT_BAL: Amount of the given credit (NT dollar): it includes both the individual consumer credit and his/her family (supplementary) credit.
- SEX: Gender (1 = male; 2 = female).
- EDUCATION: Education (1 = graduate school; 2 = university; 3 = high school; 4 = others).
- MARRIAGE: Marital status (1 = married; 2 = single; 3 = others).
- AGE: Age (year).
- PAY_1 - PAY_6: History of past payment. We tracked the past monthly payment records (from April to September, 2005) as follows: PAY_1 = the repayment status in September, 2005; PAY_2 = the repayment status in August, 2005; . . .;PAY_6 = the repayment status in April, 2005. The measurement scale for the repayment status is: -1 = pay duly; 1 = payment delay for one month; 2 = payment delay for two months; . . .; 8 = payment delay for eight months; 9 = payment delay for nine months and above.
- BILL_AMT1 - BILL_AMT6: Amount of bill statement (NT dollar). BILL_AMT1 = amount of bill statement in September, 2005; BILL_AMT2 = amount of bill statement in August, 2005; . . .; BILL_AMT6 = amount of bill statement in April, 2005. 
- PAY_AMT1 - PAY_AMT6 : Amount of previous payment (NT dollar). X18 = amount paid in September, 2005; X19 = amount paid in August, 2005; . . .;PAY_AMT6 = amount paid in April, 2005.

## 🧮 Methodology
Models: Logistic Regression, Support Vector Machine, Random Forest, XGBoost and Multilayer Perceptron

For evaluating classification performance, we’ll use standard metrics like the confusion‑matrix error rate, ROC curve, and AUC. To assess how well each model’s predicted probabilities match actual default rates, we’ll plot the observed default frequency (Y) against the model’s predicted probability (X) for each of the six methods. We’ll then fit a simple linear regression (Y = A + B·X) to each scatter plot — the model with an intercept (A) nearest zero, a slope (B) closest to one, and the highest R² will be deemed the best calibrated.

- Classification metrics + ROC-AUC
- Calibration metrics (sorting-smoothing curve)


## 📂 Repo Structure

    ├── data/
    ├── notebooks/
    ├── src/
    └── README.md


## ⚙️ Setup



## 📈 Results
| Metric | Value |
|--------|-------|
| PD AUC | 0.82 |
| LGD | 30% |

<!-- ## 📋 Next Steps
- Build downturn LGD model  
- Automate monthly data refresh   -->

## 📚 References
