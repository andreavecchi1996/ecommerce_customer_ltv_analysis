# E-commerce customer lifetime value analysis
### Project Overview & Business Value
Fecom Inc. is an e‑commerce marketplace with many one‑time buyers. The company wants to reduce churn and stop wasting marketing budget on low‑value customers. This project utilises its CRM data to identify which countries and sellers attract customers who return (for second orders) and generate the highest lifetime revenue, allowing Fecom to determine where to allocate spending and where to invest more.


Key Questions Answered:
1. Which countries have the highest percentage of returning customers?
2. Which countries generate the highest lifetime revenue per customer?  
3. Which product categories drive lifetime revenue in top markets?

The SQL queries (data quality checks, business questions and charts) are contained in this Jupyter notebook [here](ecommerce_customer_ltv_analysis.ipynb).

# Data Structure & Initial Checks
This analysis uses four tables from Fecom Inc.'s BigQuery CRM: customer_list, orders, order_items, and products, with a total row count of roughly 300k records.

<img width="656" height="598" alt="Image" src="https://github.com/user-attachments/assets/0a826770-15af-48c9-a48c-02ab8cdf0881" />

Before analysis, the BigQuery tables were loaded into Jupyter notebooks to verify correct data ingestion and format. Quality checks and initial SQL queries for exploration are included in the notebook in the [Data Selection](ecommerce_customer_ltv_analysis.ipynb#data-selection) section.

# Executive Summary
### Overview of Findings
Finland and Croatia currently have the highest share of customers who place at least a second order, with Finland above 5% returning customer rate.

However, returning customer percentage alone does not indicate customer value. Countries with high return rates but low order volume or low revenue may not justify increased marketing investment.

<img width="640" height="453" alt="Image" src="https://github.com/user-attachments/assets/4a3abc65-04f5-4e39-98e5-02d2b5971c41" />

















---
https://www.kaggle.com/datasets/cemeraan/fecom-inc-e-com-marketplace-orders-data-crm

