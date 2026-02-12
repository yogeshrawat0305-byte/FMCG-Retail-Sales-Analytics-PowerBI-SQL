# Project Overview

This project is an end-to-end Retail Sales Analytics solution built using MySQL and Power BI.
The objective is to analyze transactional sales data (100,000+ rows) and generate actionable business insights such as sales trends, product performance, location analysis, and time-based performance metrics.
# The solution demonstrates strong fundamentals in:

SQL (Advanced Queries, Window Functions)
Data Cleaning & Transformation
Business KPI Analysis
Retail/FMCG-style reporting
Power BI Data Modeling (Star Schema)
DAX & Performance Optimization

# Dataset Information
The dataset contains transactional-level sales data with the following fields:
transaction_id
transaction_date
transaction_time
transaction_qty
unit_price
store_location
product_category
product_type
product_detail
Total records: 100,000+ rows

# Data Cleaning & Preparation (SQL)
# Performed the following   transformations:

Converted transaction_date to proper DATE format
Converted transaction_time to TIME format
Modified column data types
Fixed column naming issues
Ensured data consistency before analysis

# Key Business KPIs Calculated

1️⃣ Total Sales
  Calculated using:
  SUM(unit_price * transaction_qty)

2️⃣ Total Orders
  COUNT(transaction_id)

3️⃣ Total Quantity Sold
  SUM(transaction_qty)

4️⃣ Month-over-Month (MoM) Growth
  Used LAG() window function
  Calculated:
  MoM Difference
  MoM Growth %
  Demonstrated analytical comparison between April and May
  
# Advanced SQL Analysis Performed

🔹 Sales by Store Location
  Identified top-performing stores
  Ranked locations by revenue

🔹 Sales by Product Category
  Revenue breakdown by:
  Coffee
  Tea
  Bakery
  Chocolate
  Packaged products

🔹 Top 10 Products
  Ranked products by total revenue
  Used ORDER BY + LIMIT

🔹 Daily Sales Analysis
  Aggregated daily revenue
  Compared each day’s sales against monthly average
  Classified days as:
  Above Average
  Below Average

🔹 Weekday vs Weekend Analysis
  Used CASE statements
  Identified performance differences between:
  Weekdays
  Weekends

🔹 Hourly Sales Trend
  Used HOUR(transaction_time)
  Identified peak sales hours

🔹 Average Daily Sales (Subquery)
  Used derived tables
  Calculated monthly average revenue

# SQL Concepts Demonstrated

Aggregate Functions (SUM, COUNT, AVG)
GROUP BY & ORDER BY
CASE Statements
Subqueries
Window Functions (LAG)
Date & Time Functions (MONTH, DAY, HOUR, DAYOFWEEK)
Data Type Conversions
Performance-aware query writing

# Power BI Implementation

Built Star Schema Data Model
Created DAX Measures for:
Total Sales
Total Orders
Total Quantity
MoM Growth %
Implemented:
Location-based dashboards
Product-level insights
Time intelligence analysis
Configured Scheduled Refresh
Optimized model performance for 100K+ records

# Business Insights Derived

Identified top-performing store locations
Found peak sales hours
Determined highest revenue-generating product categories
Observed strong MoM growth trend
Compared weekday vs weekend performance

# Tools Used

MySQL
Power BI Desktop
Power BI Service
DAX
Data Modeling (Star Schema)
