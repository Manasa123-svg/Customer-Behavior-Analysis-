# Customer-Behavior-Analysis-

#  End-to-End Customer Shopping Behavior Analytics

# Project Overview & Objective

This project established a complete data engineering and analytics pipeline to evaluate the shopping habits of 3,900 customers. The primary objective was to transform raw transaction data into actionable business intelligence, enabling stakeholders to identify high-value demographics, optimize inventory based on category performance, and assess the effectiveness of subscription and discount strategies.


**Data Preparation,Modeling & Exploratory Data Analysis (Python):** Clean and transform the raw dataset for analysis.

**Data Analysis (SQL):** Simulate business transactions, and run queries to extract insights on customer segments, loyalty, and purchase drivers.

**Visualization & Insights (Power BI):** Build an interactive dashboard that highlights key patterns and trends, enabling stakeholders to make data-driven decisions.

# Technology Stack

**Data Processing (ETL):** Python (Pandas, NumPy)
**Database Management:** PostgreSQL (SQLAlchemy, Psycopg2)
**Data Analysis:** Advanced SQL
**Visualization:** Power BI

# Methodology

**Phase 1:** ETL & Feature Engineering (Python)

The project began with a Python script to ingest and scrub raw CSV data. Key transformations included:
**Data Quality:** Imputed missing values in the Review Rating column using the median rating specific to each product category to ensure statistical accuracy.
Standardization: Renamed columns to snake_case for SQL compatibility and eliminated redundant features (dropping promo_code_used in favor of discount_applied).

# Feature Engineering:
**Age Segmentation:** Created a new age_group variable to categorize customers into Young Adult, Adult, Middle-aged, and Senior cohorts.

**Frequency Mapping:** Converted string-based frequencies (e.g., "Fortnightly") into numeric values (purchase_frequency_days) to enable time-based calculations.
Loading: Orchestrated a pipeline using SQLAlchemy to load the refined dataset into a local PostgreSQL database.

**Phase 2:** Data Analysis & Logic (SQL)

Once the data was warehoused, complex SQL queries were executed to derive insights:

**Customer Segmentation:** Utilized CTEs and CASE logic to classify customers as New, Returning, or Loyal based on purchase history.

**Product Performance:** Applied Window Functions (ROW_NUMBER, PARTITION BY) to rank the top 3 best-selling items within every category.

**Strategic Metrics:** Calculated revenue contributions by gender and age, and analyzed the correlation between shipping types (Standard vs. Express) and average order value.

**Phase 3:** Interactive Reporting (Power BI)

The final phase involved building a self-service dashboard to visualize the findings:

**KPI Tracking:** Displayed high-level metrics including $233K Total Revenue, 3.9K Customers, and an Avg Rating of 3.75.

**Dynamic Filtering:** Enabled slicers for Gender, Shipping Type, and Subscription Status to allow for granular analysis.

**Visual Storytelling:** Used funnel charts to show category sales volume and bar charts to compare revenue across age demographics.

# Technology Stack

**Data Processing (ETL):** Python (Pandas, NumPy)
**Database Management:** PostgreSQL (SQLAlchemy, Psycopg2)
**Data Analysis:** Advanced SQL
**Visualization:** Power BI

# Key Business Insights

**Demographic Dominance:** The Young Adult age group is the highest revenue contributor ($62K), suggesting that marketing campaigns should be tailored to younger audiences.

**Category Drivers:** Clothing is the dominant product category ($104K), generating significantly more revenue than Footwear or Outerwear, indicating where inventory budget should be prioritized.

**Subscription Opportunity:** Only 26.88% of customers are currently subscribers. With nearly 73% of the user base unsubscribed, there is a massive opportunity to target "Returning" customers with loyalty incentives to drive recurring revenue.

**Customer Satisfaction:** The average review rating of 3.75/5 indicates a generally positive sentiment, though specific sub-categories identified in SQL analysis may require quality control improvements.

**Subscription Opportunity:** Only 26.88% of customers are currently subscribers. With nearly 73% of the user base unsubscribed, there is a massive opportunity to target "Returning" customers with loyalty incentives to drive recurring revenue.

**Customer Satisfaction:** The average review rating of 3.75/5 indicates a generally positive sentiment, though specific sub-categories identified in SQL analysis may require quality control improvements
