# E-commerce customer lifetime revenue analysis
### Project Overview & Business Value
Fecom Inc. is an e‑commerce marketplace with many one‑time buyers. The company wants to reduce churn and stop wasting marketing budget on low‑value customers. This project utilises its CRM data to identify which countries and products attract customers who return (for second orders) and generate the highest lifetime revenue, allowing Fecom to determine where to allocate spending and where to invest more.


Key Questions Answered:
1. Which countries have the highest percentage of returning customers?
2. Which countries generate the highest lifetime revenue per customer?  
3. Which product categories drive lifetime revenue in top markets?

The SQL queries (data quality checks, business questions and charts) are contained in this Jupyter notebook [here](ecommerce_customer_ltr_analysis_SQL.ipynb).

# Data Structure & Initial Checks
This analysis uses four tables from Fecom Inc.'s BigQuery CRM: customer_list, orders, order_items, and products, with a total row count of roughly 300k records.

<img width="656" height="598" alt="Image" src="https://github.com/user-attachments/assets/0a826770-15af-48c9-a48c-02ab8cdf0881" />

Before analysis, the BigQuery tables were loaded into Jupyter notebooks to verify correct data ingestion and format. Quality checks and initial SQL queries for exploration are included in the notebook in the [Data Selection](ecommerce_customer_ltr_analysis_SQL.ipynb#data_selection) section.

# Executive Summary
## Overview of Findings

### Which countries have the highest percentage of returning customers?
  
Finland and Croatia currently have the highest share of customers who place at least a second order, with Finland above 5% returning customer rate.

<img width="640" height="453" alt="Image" src="https://github.com/user-attachments/assets/db5df72e-4f47-4228-9246-67e6a71079a0" />

### Which countries generate the highest lifetime revenue per customer (LTR)?
  
Based on this query, Slovakia, Luxembourg, and Finland have the highest lifetime revenue per customer. Slovakia stands out because it combines a high average LTR with a relatively large customer base (around 530 customers) and a total revenue of about 115k, compared with the much smaller bases in Luxembourg and Finland.

<img width="651" height="453" alt="Image" src="https://github.com/user-attachments/assets/fb0f88bd-150e-4ab4-a40d-2b4755f60011" />



<img width="631" height="433" alt="Image" src="https://github.com/user-attachments/assets/bfaa4b95-2bd5-4bff-8e6c-7fcf3baf2065" />
<img width="631" height="433" alt="Image" src="https://github.com/user-attachments/assets/7c28db8a-b34c-45da-8671-0d38aa8f8625" />



### Which product categories drive lifetime revenue in top markets?
Health_Beauty and Watches_Gifts are the top lifetime revenue generating product categories.


<img width="709" height="433" alt="Image" src="https://github.com/user-attachments/assets/66936d62-8c0b-4701-a837-cf2a3808cd40" />
<img width="709" height="453" alt="Image" src="https://github.com/user-attachments/assets/ddda3aa1-72fd-4910-bd6a-b7b376ee534e" />

## Recommendation
Based on the uncovered insights, the following recommendations have been provided:

Finland and Croatia currently have the highest share of customers placing at least a second order, with Finland exceeding a 5% returning-customer rate. However, the return rate alone does not guarantee high customer value; countries with strong repeat behaviour but low order volume or revenue are not necessarily priority markets for additional spending.
​

Countries with the highest lifetime revenue per customer are Slovakia, Luxembourg, and Finland, with Slovakia standing out by combining a high average LTR with a relatively large customer base (around 530 customers) and total revenue of about €115k, while Luxembourg and Finland reach similar LTR levels on much smaller bases.
​

Taking both scale and value into account, the recommended focus markets are:

- Portugal: very high total revenue and many customers, with only a small gap in average LTR versus the very top countries.
- Sweden: high total revenue and large customer base, mid returning %, slightly lower LTR.
- Denmark: solid revenue and customer volume, with a stronger LTR than Sweden.
- Slovakia: highest LTR, plus a decent customer base and strong total revenue.

Within these priority markets, Health_Beauty and Watches_Gifts are the top lifetime‑revenue‑generating product categories. Fecom should focus on upsell and cross‑sell programs around these categories: for Health_Beauty, offer discounted complementary items when a customer initially buys only one product (classic cross‑sell); for Watches_Gifts, target existing watch buyers with higher‑end models and accessories as upsell opportunities to grow LTR efficiently.
​


















---
## The dataset
https://www.kaggle.com/datasets/cemeraan/fecom-inc-e-com-marketplace-orders-data-crm
