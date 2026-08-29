# Churn Analysis & Customer Intelligence

## Overview

An end-to-end customer churn analytics project for an OTT subscription
platform. The project integrates customer, subscription, and support
data from multiple relational tables to identify churn patterns,
high-risk customer segments, and revenue impact.

## Tech Stack

-   Python
-   Pandas
-   NumPy
-   SQLite3
-   SQL
-   Matplotlib
-   Seaborn
-   Jupyter Notebook

## Dataset

The analysis uses a relational database named `customer_churn`
containing three main tables:

### `db_customer`

-   customerid
-   name
-   country
-   state
-   gender
-   dob
-   interests
-   pincode

### `db_subscription`

-   customerid
-   subscription_start_date
-   subscription_type
-   renewal_date
-   plan_type
-   contract_type
-   cancellation_date
-   cancellation_reason
-   monthly_charges
-   cltv
-   churn_score

### `db_support`

-   customerid
-   complaint_date
-   escalations
-   csat_score
-   comment

## Project Workflow

1.  Connected the SQL database to Python using Pandas and SQLite3.
2.  Imported multi-table data using SQL queries.
3.  Performed data cleaning using Pandas and NumPy.
4.  Handled data types, column selection, missing/null values and data
    quality checks.
5.  Performed feature engineering and created calculated columns.
6.  Conducted exploratory data analysis using aggregation, group-by
    operations and pivot tables.
7.  Created visualizations using Matplotlib and Seaborn.
8.  Generated business insights and recommended retention actions.

## Key Metrics

The project calculated 20+ KPIs, including:

-   Churn Rate
-   Retention Rate
-   Churn by Plan Type
-   Churn by State
-   ARPU
-   Average Customer Tenure
-   Revenue at Risk
-   Escalation Rate
-   Average Complaints per Customer
-   Escalations → Churn correlation

## Key Findings

-   **Overall churn rate:** 28.6%
-   **Retention rate:** 71.4%
-   **Monthly-contract churn:** 55.6%
-   **Annual-contract churn:** 8.3%
-   **Average customer tenure:** 1,451 days
-   **ARPU:** Rs 18.8
-   **Total revenue:** 395
-   **Revenue loss due to churn:** 74
-   **CLTV lost:** 2,047
-   **Percentage revenue loss:** 18%
-   **Most affected state:** Karnataka
-   **Highest churn month:** September 2024
-   Most churn came from the **Basic subscription plan**.
-   Monthly-contract subscribers had substantially higher churn than
    annual-contract subscribers.

The monthly vs annual churn rates were **55.6% vs 8.3%**, respectively.

## Risk Scoring & Segmentation

A multi-dimensional churn risk analysis was performed using subscription
tenure, plan type and support escalation signals across the three
relational tables.

Customers were segmented into risk tiers using composite churn scores.
Customers with **High** and **Medium** churn risk were identified as
priority groups for retention efforts.

## Support & Cancellation Analysis

Support data was combined with subscription information to analyze the
relationship between complaints, escalations, CSAT and churn.

Cancellation drivers considered in the analysis included:

-   Competitor switching
-   Pricing sensitivity
-   Content dissatisfaction
-   Support-related issues

## Business Recommendations

Based on the analysis:

-   Investigate the increase in churn observed in Karnataka.
-   Investigate whether pricing or product changes affected the Basic
    plan, particularly around September 2024.
-   Review competitor activity and switching behavior.
-   Prioritize customers with High and Medium churn risk.
-   Consider customer LTV when prioritizing retention efforts.
-   Reach out to high-risk customers through email, SMS or calls to
    address issues and improve retention.

## Project Structure

``` text
churn_analysis/
│
├── churn_analysis.ipynb
├── README.md
└── Data/
    └── customer_churn.db
```

## Skills Demonstrated

-   Python for data analytics
-   SQL and relational data extraction
-   Data cleaning
-   Feature engineering
-   Exploratory Data Analysis (EDA)
-   Data visualization
-   Customer segmentation
-   Churn analysis
-   Business KPI analysis
-   Translating data findings into actionable recommendations
