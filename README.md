# 🍕 Power BI Pizza Sales Dashboard with MySQL & Excel

This project is an end-to-end **Sales Analytics Dashboard** built using **Power BI**, **MySQL**, and **Excel**. It visualizes pizza sales data to uncover key insights on performance, customer behavior, and product trends — helping businesses drive strategic decisions with data.

---

## Tools & Technologies Used

-  **Power BI** – for data visualization and dashboard creation
-  **MySQL** – for data querying, aggregation, and transformation
-  **Excel** – used for preliminary cleaning and data checks
-  **DAX (Data Analysis Expressions)** – to create calculated measures in Power BI

---

## 📁 Files Included

| File | Description |
|------|-------------|
| `pizza_sales.csv` | Raw transactional pizza sales data |
| `PIZZA PROJECT CODES.docx` | SQL queries used in MySQL |
| `dax_measures.txt` | DAX formulas used in the dashboard |
| `screenshots/dashboard_overview.png` | Dashboard visuals |
| `README.md` | Project documentation |

---

## 🧠 Key Metrics & KPIs

### ✅ SQL-Based Calculations (MySQL)
```sql
-- Total Revenue
SELECT SUM(total_price) AS Total_Revenue FROM pizza_sales.pizza_sales;

-- Average Order Value
SELECT SUM(total_price)/COUNT(DISTINCT order_id) AS Average_Order_Value FROM pizza_sales.pizza_sales;

-- Total Pizzas Sold
SELECT SUM(quantity) AS Total_Pizzas_Sold FROM pizza_sales.pizza_sales;

-- Total Orders
SELECT COUNT(DISTINCT order_id) AS Total_Orders FROM pizza_sales.pizza_sales;

-- Avg. Pizzas Per Order
SELECT ROUND(SUM(quantity) / COUNT(DISTINCT order_id), 2) AS Avg_Pizzas_per_order FROM pizza_sales.pizza_sales;

