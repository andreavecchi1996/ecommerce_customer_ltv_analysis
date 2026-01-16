# E-commerce customer lifetime value analysis
### Project Overview & Business Value
Fecom Inc. is an e‑commerce marketplace with many one‑time buyers. The company wants to reduce churn and stop wasting marketing budget on low‑value customers. This project uses its CRM data to identify which countries and sellers attract customers who return (second orders) and generate the highest lifetime revenue, so Fecom can decide where to cut spending and where to invest more.


Key Questions Answered:
1. Which countries have the highest percentage of returning customers?
2. Which countries generate the highest lifetime revenue per customer?  
3. Which product categories drive lifetime revenue in top markets?

The SQL queries (data quality checks, business questions and charts) are contained in this Jupyter notebook [here](ecommerce_customer_ltv_analysis.ipynb)

---
### Data Structure & Initial Checks
This analysis uses four tables from Fecom Inc.'s CRM: customer_list, orders, order_items, and products, with a total row count of roughly 300k records 




---
BigQuery is used as the main data warehouse and for all heavy transformations; pandas is used in the notebook for quick inspection and visualisation.
---
https://www.kaggle.com/datasets/cemeraan/fecom-inc-e-com-marketplace-orders-data-crm

