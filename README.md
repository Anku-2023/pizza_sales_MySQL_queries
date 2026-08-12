 🍕 Pizza Sales Analysis — SQL Portfolio Project

📌 Project Overview

This project analyzes a pizza sales dataset using **MySQL** to extract meaningful business insights related to sales performance, customer ordering patterns, product popularity, revenue contribution, and category-level performance.

The project was designed as a practical **SQL Analytics portfolio project**, progressing from basic SQL queries to advanced analytical techniques such as cumulative revenue analysis and category-wise ranking.

---
 🎯 Business Objectives

The analysis aims to answer key business questions such as:

* How many orders were placed?
* How much revenue was generated?
* Which pizzas and pizza sizes are most popular?
* Which pizza categories generate the most sales?
* What are the busiest ordering hours?
* Which pizza types generate the highest revenue?
* What percentage of total revenue does each pizza contribute?
* How does revenue accumulate over time?
* What are the top-performing pizzas within each category?

---

## 🗂️ Project Structure

```text
Pizza-Sales-SQL-Analysis/
│
├── README.md
│
├── data/
│   ├── orders.csv
│   ├── order_details.csv
│   ├── pizzas.csv
│   └── pizza_types.csv
│
├── sql/
│   ├── database_setup.sql
│   ├── basic_analysis.sql
│   ├── intermediate_analysis.sql
│   └── advanced_analysis.sql
│
└── insights/
    └── business_insights.md
```

---

## 🛠️ Tools & Technologies

* **MySQL**
* **MySQL Workbench**
* SQL
* Git & GitHub

### SQL Concepts Used

* `SELECT`
* `WHERE`
* `GROUP BY`
* `ORDER BY`
* `LIMIT`
* Aggregate Functions

  * `SUM()`
  * `COUNT()`
  * `AVG()`
  * `MAX()`
* `JOIN`
* `CASE`
* Date & Time Functions
* Subqueries
* Common Table Expressions (CTEs)
* Window Functions
* Ranking
* Cumulative calculations

---

# 📊 Analysis Performed

## 1. Basic Analysis

The first stage focuses on understanding overall sales performance and identifying the most popular products.

### Questions Answered

1. Total number of orders placed
2. Total revenue generated from pizza sales
3. Highest-priced pizza
4. Most commonly ordered pizza size
5. Top 5 most ordered pizza types by quantity

These queries establish the fundamental sales KPIs and product-level performance.

---

## 2. Intermediate Analysis

The second stage combines multiple tables to understand customer ordering behavior and sales patterns.

### Questions Answered

1. Total quantity of pizzas ordered by category
2. Distribution of orders by hour of the day
3. Category-wise distribution of pizzas
4. Average number of pizzas ordered per day
5. Top 3 pizza types based on revenue

This stage demonstrates the use of **table joins, grouping, aggregation, and date/time analysis**.

---

## 3. Advanced Analysis

The final stage focuses on deeper revenue and product-performance analysis.

### Questions Answered

1. Percentage contribution of each pizza type to total revenue
2. Cumulative revenue generated over time
3. Top 3 pizza types by revenue within each pizza category

These analyses use more advanced SQL techniques including **window functions, ranking, and cumulative calculations**.

---

# 🗄️ Database Schema

The project uses a relational database consisting of four primary tables:

```text
                 ┌──────────────┐
                 │    orders    │
                 ├──────────────┤
                 │ order_id     │
                 │ order_date   │
                 │ order_time   │
                 └──────┬───────┘
                        │
                        │ order_id
                        ▼
              ┌───────────────────┐
              │  order_details    │
              ├───────────────────┤
              │ order_details_id  │
              │ order_id          │
              │ pizza_id          │
              │ quantity           │
              └─────────┬─────────┘
                        │
                        │ pizza_id
                        ▼
                 ┌──────────────┐
                 │    pizzas    │
                 ├──────────────┤
                 │ pizza_id     │
                 │ pizza_type_id│
                 │ size         │
                 │ price        │
                 └──────┬───────┘
                        │
                        │ pizza_type_id
                        ▼
              ┌──────────────────┐
              │   pizza_types    │
              ├──────────────────┤
              │ pizza_type_id    │
              │ name             │
              │ category         │
              │ ingredients      │
              └──────────────────┘
```

This relational structure allows sales transactions to be connected with pizza details and category information.

---

# 🔍 Key Analytical Areas

### 💰 Revenue Analysis

* Total revenue
* Revenue by pizza type
* Revenue contribution %
* Cumulative revenue
* Revenue ranking

### 🍕 Product Analysis

* Most ordered pizza types
* Highest-priced pizza
* Top revenue-generating pizzas
* Category-level performance
* Top pizzas within each category

### ⏰ Time Analysis

* Orders by hour
* Orders by date
* Average daily pizza orders
* Revenue progression over time

### 📦 Category Analysis

* Pizza quantity by category
* Category-wise distribution
* Top-performing pizzas within each category

---

# 💡 Business Insights

The analysis can help a pizza business understand:

* Which products drive the majority of sales
* Which pizzas contribute most to revenue
* Which categories have the strongest demand
* When customers are most likely to place orders
* Which products may deserve additional promotion
* Which products have relatively low demand
* How sales performance changes over time

These insights can support decisions related to **menu optimization, promotions, inventory planning, and staffing**.

---

# 🚀 How to Run the Project

### 1. Install MySQL

Install **MySQL Server** and **MySQL Workbench**.

### 2. Create the Database

Run the database setup SQL script:

```sql
CREATE DATABASE pizzahut;

USE pizzahut;
```

### 3. Create the Tables

Run the table creation queries for:

```text
orders
order_details
pizzas
pizza_types
```

### 4. Load the Dataset

Import the corresponding CSV files into the MySQL tables.

### 5. Run the Analysis

Execute the SQL scripts in the following order:

```text
01_database_setup.sql
02_basic_analysis.sql
03_intermediate_analysis.sql
04_advanced_analysis.sql
```

---

# 📈 Skills Demonstrated

This project demonstrates practical ability in:

**SQL & Database**

* Relational database design
* Data querying
* Data aggregation
* Multi-table joins
* Data filtering
* Date/time analysis

**Analytics**

* KPI calculation
* Revenue analysis
* Product performance analysis
* Trend analysis
* Category analysis
* Ranking analysis

**Advanced SQL**

* CTEs
* Subqueries
* Window functions
* `RANK()` / `DENSE_RANK()`
* Running totals
* Percentage calculations

---

# 👨‍💻 Author

**Vikash Samal**

This project was created as part of a practical SQL and data analytics portfolio to demonstrate the ability to transform transactional data into actionable business insights.
