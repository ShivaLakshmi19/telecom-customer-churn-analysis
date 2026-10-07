# Customer Churn Analysis (Telecom)

By Shiva Lakshmi Padala

## Problem
A telecom company is losing customers. Which customers leave, why, and what should the company do to keep them?

## Dataset
Telco Customer Churn (IBM sample dataset): about 7,000 customers, 21 columns. The target column is `Churn` (Yes/No).

## Tools
Python, pandas, Matplotlib, scikit-learn, Google Colab

## Approach
1. Loaded and inspected the data
2. Cleaned it: converted `TotalCharges` to numeric, dropped 11 rows of brand-new customers who had not been billed yet, and checked for duplicates
3. Measured the overall churn rate
4. Compared churn by contract type, internet service, payment method, tech support, senior citizen status, and tenure
5. Identified the highest-risk customer segment and estimated revenue at risk
6. Built a simple logistic regression model as an extra

## Key findings
- Overall churn rate: 26.6%
- Month-to-month customers churn at 42.7%, versus 11.3% on one-year and 2.8% on two-year contracts
- Churn is highest in the first 12 months of tenure (47.7%) and falls to 9.5% after 4 years
- Fiber optic customers churn at 41.9%, versus 19.0% for DSL
- Customers without tech support churn at 41.6%, versus 15.2% for those with it
- Highest-risk segment (month-to-month + fiber optic + tenure of 12 months or less): 70.2% churn
- Customers who churned account for 30.5% of total monthly revenue
- Logistic regression accuracy: 80.5% (the majority-class baseline is about 73%)

## Recommendations
1. Offer incentives to move month-to-month customers to longer contracts
2. Run an onboarding and check-in program for first-year customers
3. Investigate fiber optic service quality and pricing
4. Bundle tech support and online security with plans
5. Target the highest-risk segment first with retention offers

## Limitations
This is a single-snapshot sample dataset, so the analysis shows associations, not proof of cause.

## How to run
1. Download `WA_Fn-UseC_-Telco-Customer-Churn.csv` from Kaggle (search "Telco Customer Churn")
2. Open `Customer_Churn_Analysis.ipynb` in Google Colab and upload the CSV
3. Run all cells
