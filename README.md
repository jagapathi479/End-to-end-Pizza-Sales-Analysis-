# 🍕 Pizza Sales Analysis — SQL & Power BI

> **End-to-End Business Intelligence Project | MSSQL Server • SQL • Power BI • DAX**

## 📌 Overview

**Pizza Sales Analysis** is an end-to-end Business Intelligence project designed to analyze pizza sales transactions and transform raw transactional data into actionable business insights.

The project uses **MSSQL Server** for data querying and analytical calculations and **Power BI** for interactive data visualization and dashboard development.

The analysis focuses on **revenue performance, order volume, product performance, pizza categories, pizza sizes, and time-based sales patterns** to provide a comprehensive view of business performance.

---

## 🎯 Business Objective

The primary objective of this project is to answer key business questions related to pizza sales performance:

* How much revenue is being generated?
* How many orders and pizzas are being sold?
* What is the average order value?
* Which pizzas generate the most revenue?
* Which products have the lowest demand?
* Which pizza categories perform best?
* Which pizza sizes are most popular?
* Which days and months generate the highest sales?
* How does sales performance change over time?

---

## 🧩 Project Scope

The project covers the complete analytics workflow:

**Transactional Data → SQL Analysis → KPI Development → Power BI Modeling → Dashboard → Business Insights**

### Key Areas

| Area       | Analysis                              |
| ---------- | ------------------------------------- |
| Revenue    | Total and average revenue performance |
| Orders     | Order volume and ordering patterns    |
| Products   | Product-level performance             |
| Categories | Category contribution to sales        |
| Size       | Customer preference by pizza size     |
| Time       | Daily and monthly sales trends        |
| Ranking    | Top and Bottom performing pizzas      |

---

# 🗂️ Dataset

The dataset contains pizza order-level transactional information covering approximately **one year of sales activity**.

### Key Fields

| Column           | Description                        |
| ---------------- | ---------------------------------- |
| `order_id`       | Unique identifier for each order   |
| `order_date`     | Date on which the order was placed |
| `order_time`     | Time of the order                  |
| `pizza_name`     | Name of the pizza                  |
| `pizza_category` | Pizza category                     |
| `pizza_size`     | Size of the pizza                  |
| `quantity`       | Number of pizzas ordered           |
| `unit_price`     | Price per pizza                    |
| `total_price`    | Total value of the transaction     |

---

# 🛠️ Technology Stack

### Database & SQL

* **Microsoft SQL Server**
* SQL
* Aggregate Functions
* JOINs
* GROUP BY
* CASE Statements
* Subqueries
* Date Functions
* Filtering & Sorting

### Business Intelligence

* **Microsoft Power BI**
* DAX
* Data Modeling
* KPI Development
* Interactive Visualizations
* Slicers & Filters

---

# 🔄 Data Analytics Workflow

```text
                  RAW TRANSACTION DATA
                           │
                           ▼
                   ┌───────────────┐
                   │ MSSQL SERVER  │
                   └───────┬───────┘
                           │
                           ▼
                  SQL DATA ANALYSIS
                           │
             ┌─────────────┼─────────────┐
             ▼             ▼             ▼
          Revenue        Orders       Products
             │             │             │
             └─────────────┼─────────────┘
                           ▼
                    KPI CALCULATIONS
                           │
                           ▼
                  POWER BI DATA MODEL
                           │
                           ▼
                INTERACTIVE DASHBOARD
                           │
                           ▼
                   BUSINESS INSIGHTS
```

---

# 📊 KPI Framework

The dashboard was designed around key sales performance indicators.

### 1. Total Revenue

Measures the overall revenue generated from pizza sales.

```text
Total Revenue = SUM(Total Price)
```

### 2. Total Orders

Measures the number of unique customer orders.

```text
Total Orders = DISTINCTCOUNT(Order ID)
```

### 3. Total Pizzas Sold

Measures the total quantity of pizzas sold.

```text
Total Pizzas Sold = SUM(Quantity)
```

### 4. Average Order Value

Measures the average revenue generated per order.

```text
AOV = Total Revenue / Total Orders
```

### 5. Average Pizzas Per Order

Measures the average number of pizzas included in each order.

```text
Average Pizzas Per Order =
Total Pizzas Sold / Total Orders
```

---

# 🧮 SQL Analysis

SQL was used as the primary analytical layer for extracting business metrics from the transactional dataset.

### Analytical techniques implemented

```sql
-- Aggregation
SUM()
COUNT()
AVG()
MIN()
MAX()

-- Data grouping
GROUP BY

-- Conditional logic
CASE WHEN

-- Table relationships
JOIN

-- Filtering
WHERE
HAVING

-- Sorting
ORDER BY

-- Time analysis
YEAR()
MONTH()
DAY()
DATENAME()
```

### Example — Revenue by Pizza Category

```sql
SELECT
    pizza_category,
    SUM(total_price) AS total_revenue
FROM pizza_sales
GROUP BY pizza_category
ORDER BY total_revenue DESC;
```

### Example — Top Performing Pizzas

```sql
SELECT TOP 5
    pizza_name,
    SUM(total_price) AS revenue
FROM pizza_sales
GROUP BY pizza_name
ORDER BY revenue DESC;
```

---

# 📈 Power BI Dashboard

The Power BI dashboard converts the SQL analysis into an interactive reporting interface.

## Dashboard Components

### Executive KPI Section

Displays:

* Total Revenue
* Total Orders
* Total Pizzas Sold
* Average Order Value
* Average Pizzas Per Order

### Sales Trend Analysis

Visualizes:

* Daily revenue
* Monthly revenue
* Daily order volume
* Monthly order volume

### Product Performance

Provides:

* Top 5 pizzas
* Bottom 5 pizzas
* Revenue by pizza
* Orders by pizza
* Quantity sold by pizza

### Category Analysis

Compares:

* Revenue by category
* Orders by category
* Quantity sold by category

### Size Analysis

Examines:

* Revenue by pizza size
* Quantity sold by size
* Order distribution by size

### Interactive Filtering

Users can dynamically explore the dashboard using:

* Pizza Category
* Pizza Size
* Pizza Name
* Date
* Time-based filters

---

# 🔍 Business Questions Answered

The dashboard enables stakeholders to quickly answer:

### Revenue & Orders

* What is the overall revenue?
* How many orders were placed?
* What is the average order value?
* How many pizzas were sold?

### Product Performance

* Which pizza generates the highest revenue?
* Which pizza has the highest order volume?
* Which products are underperforming?
* Which products should receive additional attention?

### Customer Ordering Patterns

* Which pizza sizes are most frequently purchased?
* What days have the highest order volume?
* What months generate the highest revenue?

### Category Performance

* Which pizza category contributes the most revenue?
* Which category has the highest quantity sold?
* How does category performance vary over time?

---

# 💡 Key Analytical Outcomes

The analysis provides a structured view of pizza sales performance across multiple dimensions.

### Product-Level Performance

Ranking pizzas by **revenue, order count, and quantity sold** makes it possible to distinguish high-demand products from underperforming products.

### Time-Based Performance

Daily and monthly analysis highlights **sales fluctuations and peak ordering periods**, supporting operational and demand-planning decisions.

### Category Performance

Comparing pizza categories provides visibility into which product groups contribute most significantly to overall sales.

### Size Preference

Pizza-size analysis provides insight into **customer purchasing preferences** and the contribution of different sizes to sales.

---

# 📐 Dashboard Design

The dashboard follows a business-oriented reporting structure:

```text
┌─────────────────────────────────────────────────────┐
│                 SALES PERFORMANCE                   │
├────────────┬────────────┬────────────┬──────────────┤
│ Revenue    │ Orders     │ Pizzas     │ Avg Order   │
├────────────┴────────────┴────────────┴──────────────┤
│                                                     │
│              DAILY / MONTHLY TRENDS                 │
│                                                     │
├─────────────────────────┬───────────────────────────┤
│  CATEGORY PERFORMANCE   │     SIZE PERFORMANCE      │
│                         │                           │
├─────────────────────────┴───────────────────────────┤
│                                                     │
│          TOP 5 / BOTTOM 5 PRODUCTS                  │
│                                                     │
└─────────────────────────────────────────────────────┘
```

---

# 📁 Repository Structure

```text
Pizza-Sales-Analysis/
│
├── Dataset/
│   └── pizza_sales.csv
│
├── SQL/
│   └── pizza_sales_analysis.sql
│
├── PowerBI/
│   └── Pizza_Sales_Dashboard.pbix
│
├── Screenshots/
│   └── dashboard.png
│
└── README.md
```

---

# 🚀 Project Highlights

* End-to-end **SQL + Power BI analytics workflow**
* **10+ analytical SQL queries**
* **6+ business KPIs**
* Product-level performance ranking
* Top 5 and Bottom 5 product analysis
* Category and size analysis
* Daily and monthly trend analysis
* Interactive Power BI dashboard
* Business-focused KPI reporting
* Multi-dimensional sales analysis

---

# 📚 Skills Demonstrated

### SQL

`MSSQL Server` `JOINs` `GROUP BY` `CASE WHEN` `Subqueries` `Aggregations` `Date Functions`

### Power BI

`DAX` `Data Modeling` `KPI Cards` `Slicers` `Interactive Dashboards` `Data Visualization`

### Analytics

`Sales Analysis` `Trend Analysis` `Product Analysis` `KPI Development` `Business Intelligence` `Data-Driven Decision Making`

---

# 🎓 Learning Outcomes

Through this project, I strengthened my ability to:

* Translate business questions into analytical SQL queries.
* Work with transactional sales data.
* Develop meaningful business KPIs.
* Perform multi-dimensional sales analysis.
* Create interactive Power BI dashboards.
* Communicate analytical findings through visual storytelling.
* Convert raw data into structured business intelligence.

---

# 👨‍💻 Author

**Jagapathi Tankala**

**Data Analyst | SQL | Python | Power BI | Excel**

📍 Andhra Pradesh, India

---

## ⭐ If you find this project useful

Feel free to **star ⭐ the repository** and explore the SQL analysis and Power BI dashboard.
