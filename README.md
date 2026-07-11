# Customer-Churn-Retention-Analysis

This project analyzes customer churn for a telecom company using Python, SQL, and Power BI. The goal of this project is to identify customer groups with higher churn risk and provide business recommendations to improve customer retention.

## Project Overview

Customer churn is an important business problem because losing customers can reduce revenue and slow business growth. In this project, I used a telecom customer churn dataset from Kaggle to understand which customer groups are more likely to leave the company.

The project follows a complete data analysis workflow:

* Downloaded the dataset from Kaggle
* Cleaned and prepared the data using Python
* Created SQL tables and wrote SQL queries for analysis
* Built an interactive Power BI dashboard
* Identified churn patterns and retention opportunities

## Business Problem

The telecom company wants to understand which customers are leaving and what customer characteristics are linked with higher churn.

The main business question is:

Which customer groups are more likely to churn, and where should the company focus its retention efforts?

* Python
* Pandas
* SQL / PostgreSQL
* Power BI
* DAX
* Power Query
* Data Modeling
* Data Visualization

## Dataset

The dataset includes customer demographic information, account details, services used, billing details, and churn status.

Main fields include:

* Customer ID
* Gender
* Senior Citizen
* Partner
* Dependents
* Tenure
* Phone Service
* Internet Service
* Online Security
* Tech Support
* Contract
* Payment Method
* Monthly Charges
* Total Charges
* Churn

## Data Cleaning Using Python

I used Python to clean and prepare the raw dataset before loading it into SQL and Power BI.

Main cleaning steps included:

* Checked the shape, column names, and dataset information
* Renamed columns to make them easier to use in SQL
* Checked missing values and duplicate records
* Converted `SeniorCitizen` from 0/1 to Yes/No
* Converted `TotalCharges` from object type to numeric
* Filled missing `TotalCharges` values with 0 because those customers had 0 tenure and were new customers
* Created new columns for analysis:

  * `tenure_group`
  * `tenure_group_order`
  * `monthly_charge_group`
  * `monthly_charge_group_order`
  * `churn_flag`
* Exported the cleaned dataset for SQL and Power BI analysis

## SQL Analysis

After cleaning the data, I used SQL to create analysis tables and answer business questions.

The cleaned data was organized into separate tables:

* `churn_data`
* `customers`
* `customer_contracts`
* `customer_services`

SQL queries were written to analyze:

* Overall churn rate
* Churn by tenure group
* Churn by contract type
* Churn by payment method
* Churn by monthly charge group
* Churn by internet service
* Churn by Online Security and Tech Support
* Churn by demographic groups
* High-risk customer segments
* Lost monthly revenue from churned customers
* Differences between churned and retained customer profiles

## Power BI Dashboard

Power BI was used to build an interactive dashboard with three report pages.

### Page 1: Customer Churn Overview

This page gives a high-level summary of customer churn.

It includes:

* Total Customers
* Churned Customers
* Retained Customers
* Churn Rate
* Lost Monthly Revenue
* Customer Churn Distribution
* Churn Rate by Tenure Group
* Churn Rate by Contract Type

**Key Insight:**
Customers in the 0–12 month tenure group have the highest churn rate at 47.44%. Month-to-month customers also show much higher churn compared with one-year and two-year contract customers.

### Page 2: Customer Churn Drivers

This page focuses on account, payment, and service factors linked with higher churn.

It includes:

* Churn Rate by Payment Method
* Churn Rate by Internet Service
* Churn Rate by Online Security
* Churn Rate by Tech Support

**Key Insight:**
Electronic check customers have the highest churn rate at 45.29%. Fiber optic customers also show high churn at 41.89%. Customers without Online Security or Tech Support have higher churn compared with customers who use these services.

### Page 3: Retention Opportunity Analysis

This page focuses on high-risk customer segments and revenue loss from churn.

It includes:

* Churn Rate by Monthly Charge Group
* Churn Rate by Tenure and Contract
* Lost Monthly Revenue by Monthly Charge Group
* Lost Monthly Revenue Breakdown

**Key Insight:**
The highest revenue-loss segment is concentrated among month-to-month customers, especially those using fiber optic service, electronic check payment, and shorter tenure. High monthly charge customers also show higher churn and revenue loss.

## Key Findings

* The overall churn rate is 26.54%.
* Customers with 0–12 months tenure have the highest churn rate at 47.44%.
* Month-to-month customers churn at 42.71%, compared with only 2.83% for two-year contract customers.
* Electronic check customers have the highest churn rate among payment methods at 45.29%.
* Fiber optic customers have a high churn rate of 41.89%.
* High monthly charge customers have a churn rate of 37.82%.
* Customers without Online Security and Tech Support show higher churn patterns.
* Month-to-month customers contribute the highest lost monthly revenue from churn.

## Business Recommendations

Based on the analysis, the company should:

* Focus retention campaigns on new customers within their first 12 months.
* Encourage month-to-month customers to move to longer-term contracts through loyalty offers or discounts.
* Review the customer experience for electronic check users.
* Review pricing, service quality, and customer expectations for fiber optic customers.
* Promote Online Security and Tech Support services to customers with higher churn risk.
* Prioritize high monthly charge customers for retention offers because they create higher revenue loss when they churn.

## Dashboard Screenshots

 Customer Churn Overview

<img width="1470" height="956" alt="Customer Churn Overview" src="https://github.com/user-attachments/assets/ff3c3690-e7e1-46a0-9937-7f5a54adad55" />

 Customer Churn Drivers

<img width="1470" height="956" alt="Customer Churn Drivers" src="https://github.com/user-attachments/assets/75ce5d33-91b3-405a-822b-38f0aa58629f" />

 Retention Opportunity Analysis

<img width="1470" height="956" alt="Retention Opportunity Analysis" src="https://github.com/user-attachments/assets/d4d04b64-04e9-41c3-ac94-a62f9662ac6e" />

## Repository Files

This repository includes:

* `cleaned_telco_churn.csv` — cleaned dataset used for analysis
* `telco_churn_cleaning.ipynb` — Python notebook for data cleaning and feature creation
* `churn_analysis_queries.sql` — SQL queries used to analyze churn patterns
* `churn_visualization.pbix` - Power BI report file

## Conclusion

This project shows how Python, SQL, and Power BI can be used together to solve a business problem. Python was used to clean and prepare the data, SQL was used to analyze churn patterns, and Power BI was used to create an interactive dashboard for business users.

The analysis found that churn is higher among new customers, month-to-month customers, electronic check users, fiber optic customers, and high monthly charge customers. These insights can help the business create better retention strategies and reduce customer loss.

