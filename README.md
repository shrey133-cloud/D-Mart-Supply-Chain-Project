# AI-Powered Supply Chain Data Analysis Dashboard

## Overview

This project demonstrates how AI-assisted analytics can be combined with SQL and PostgreSQL to analyze supply chain operations. The dashboard provides insights into customer performance, product sales, order fulfillment, and delivery metrics using Quadratic AI connected to a Supabase PostgreSQL database.

The project enables business users to explore large datasets with natural language and SQL queries while generating meaningful visualizations.

---

## Features

- Customer sales analysis
- Product performance tracking
- Order trend analysis
- On-Time (OT) delivery analysis
- In-Full (IF) delivery analysis
- OTIF (On-Time In-Full) KPI tracking
- AI-assisted SQL query generation
- Interactive spreadsheet-based analytics
- PostgreSQL database integration

---

## Tech Stack

- Quadratic AI
- PostgreSQL
- Supabase
- SQL
- Spreadsheet Analytics

---

## Database Schema

The project uses the following tables:

- dim_customers
- dim_products
- dim_targets_orders
- fact_order_line
- fact_aggregate

These tables follow a star schema commonly used in data warehousing.

---

## Key Business Questions

- Which customers generated the highest revenue?
- Which products are the best-performing?
- What is the monthly order trend?
- What is the overall OTIF percentage?
- Which customers have poor delivery performance?
- How do products perform across different cities?
- Which orders were delivered on time and in full?

---

## KPIs

- Total Orders
- Total Customers
- Total Products
- Revenue
- On-Time Delivery %
- In-Full Delivery %
- OTIF %
- Monthly Orders
- Customer-wise Sales

---

## Project Workflow

1. Import CSV datasets into Supabase.
2. Create relational tables.
3. Connect Supabase to Quadratic AI.
4. Execute SQL queries.
5. Generate insights using AI.
6. Build interactive dashboards.
7. Analyze business KPIs.

---

## Project Structure

```
SupplyChain-Analytics/
│
├── data/
│   ├── dim_customers.csv
│   ├── dim_products.csv
│   ├── dim_targets_orders.csv
│   ├── fact_order_line.csv
│   └── fact_aggregate.csv
│
├── sql/
│   ├── customer_queries.sql
│   ├── product_queries.sql
│   └── dashboard_queries.sql
│
├── screenshots/
│
├── README.md
│
└── LICENSE
```

---

## Sample SQL Query

```sql
SELECT
    customer_name,
    COUNT(order_id) AS total_orders
FROM fact_order_line
JOIN dim_customers
ON fact_order_line.customer_id = dim_customers.customer_id
GROUP BY customer_name
ORDER BY total_orders DESC;
```

---

## Learning Outcomes

- PostgreSQL Database Management
- SQL Query Writing
- Data Warehousing Concepts
- Supply Chain Analytics
- AI-assisted Data Analysis
- Business Intelligence
- KPI Reporting

---
## Author

**Shreya Mittal**

B.Tech (Information Technology)

Skills: SQL, Python, PostgreSQL, AI Prompt Engineering, Data Analysis, Supabase, Quadratic AI

