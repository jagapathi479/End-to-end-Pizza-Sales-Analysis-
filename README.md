🍕 Pizza Sales Analysis

An end-to-end Sales Analytics and Business Intelligence project using MSSQL Server and Power BI to analyze pizza sales transactions, uncover sales trends, evaluate product performance, and build an interactive business dashboard.

📌 Project Overview

This project analyzes one year of pizza sales transaction data to understand revenue performance, order patterns, product demand, and customer ordering behavior.

The project combines SQL-based data analysis with Power BI visualization to convert raw transactional data into meaningful business insights.

🛠️ Tools & Technologies
MSSQL Server – Data querying and analysis
SQL – Data aggregation, filtering, joins, and KPI calculations
Power BI – Interactive dashboard and visualization
DAX – KPI and calculated measure creation
📊 Key KPIs

The dashboard tracks important sales performance indicators including:

Total Revenue
Total Orders
Total Pizzas Sold
Average Order Value (AOV)
Average Pizzas per Order
Daily & Monthly Sales Performance
🔍 Analysis Performed
1. Sales Trend Analysis
Evaluated daily and monthly order patterns.
Identified peak sales periods.
Compared sales performance across different time periods.
2. Product Analysis
Evaluated pizza performance based on:
Revenue
Orders
Quantity sold
Identified Top 5 and Bottom 5 pizzas.
3. Category Analysis
Compared sales performance across pizza categories.
Determined which categories generated higher revenue and order volume.
4. Size Analysis
Examined customer preference across different pizza sizes.
Compared quantity sold and revenue by pizza size.
5. Time-Based Analysis
Analyzed sales by:
Day of week
Month
Order volume
Revenue
📈 Power BI Dashboard

The interactive dashboard provides:

KPI cards
Daily sales trend
Monthly sales trend
Sales by pizza category
Sales by pizza size
Top 5 pizzas
Bottom 5 pizzas
Interactive slicers and filters
🗄️ SQL Analysis

SQL was used to calculate business metrics and perform analytical queries using:

JOIN
GROUP BY
ORDER BY
CASE WHEN
Aggregate Functions
Date Functions
Subqueries
WHERE
HAVING

Example KPI calculation:

SELECT 
    SUM(total_price) AS Total_Revenue,
    COUNT(DISTINCT order_id) AS Total_Orders,
    SUM(quantity) AS Total_Pizzas_Sold
FROM pizza_sales;
💡 Key Insights

The analysis helps answer business questions such as:

Which pizzas generate the highest revenue?
Which pizzas have the lowest demand?
Which pizza category performs best?
Which pizza size is most frequently ordered?
Which days generate the most orders?
Which months have the highest sales?
What is the average value of each customer order?
📁 Project Structure
Pizza-Sales-Analysis/
│
├── Dataset/
│   └── pizza_sales.csv
│
├── SQL/
│   └── pizza_sales_queries.sql
│
├── PowerBI/
│   └── pizza_sales_dashboard.pbix
│
├── Dashboard/
│   └── pizza_sales_dashboard.png
│
└── README.md

🔄 Project Workflow
Raw Sales Data
      ↓
MSSQL Server
      ↓
SQL Data Analysis
      ↓
KPI & Business Metrics
      ↓
Power BI
      ↓
Interactive Dashboard
      ↓
Business Insights
🎯 Business Value

This project demonstrates practical skills in:

SQL Data Analysis
Business Intelligence
KPI Development
Data Visualization
Sales Performance Analysis
Trend Analysis
Product Performance Analysis
Interactive Dashboard Development
👨‍💻 Author

Jagapathi Tankala

Skills: SQL | Python | Power BI | Excel | Data Analytics
