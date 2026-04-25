# SalesScope-Business-Performance-Analytics-using-SQL-Powerbi

## 📌 Project Overview

This project is a comprehensive analysis of sales data using PowerBI and SQL. It provides valuable insights into sales performance, trends, and patterns, enabling informed decision-making.

Table of Contents Project Description Getting Started Data Sources Data Preparation Analysis Visualizations Conclusion

This project aims to analyze and visualize sales data to extract meaningful insights. We used PowerBI for data visualization and SQL for data extraction, transformation, and loading (ETL).

---

## 🎯 Project Objectives

- Analyze overall sales revenue and quantity performance  
- Identify top customers and top-selling products  
- Compare revenue across different markets/zones  
- Track monthly and yearly sales trends  
- Understand customer contribution to revenue  
- Generate actionable insights for business growth  

---

## 📈 Key Metrics Used

- *Revenue* – Total realized revenue from sales transactions  
- *Sales Qty* – Total quantity sold  
- *Revenue Contribution %* – Customer contribution to total revenue  
- *Top Customers* – Highest revenue generating customers  
- *Top Products* – Best performing products  
- *Market Revenue* – Revenue by city/zone/market  

---

## 📊 Dashboard Features

✅ KPI cards for Revenue & Sales Qty  
✅ Revenue trend over time  
✅ Sales quantity by year  
✅ Revenue by market / zone  
✅ Revenue by customer type  
✅ Revenue by product type  
✅ Top 5 Customers  
✅ Top 5 Products  
✅ Dynamic slicers & filters  

---

## 🛠 Tools & Technologies

- Power BI Desktop  
- SQL (MySQL)  
- DAX (Data Analysis Expressions)  
- Power Query  
- Data Modeling  

---

## 🗂 Dataset Tables Used

- customers  
- dates  
- markets  
- products  
- transactions  

---

## 💻 SQL Analysis Performed

Analyzed business sales data using SQL queries such as:

- Total transaction count  
- Revenue by currency  
- Revenue by customer type  
- Revenue by market  
- Revenue by product type  
- Top 5 customers by sales  
- Monthly sales trend  
- Daily sales quantity  
- Average sales amount  
- Product performance analysis  

---

## 📐 DAX Measures Used

```DAX
Revenue = SUM(transactions[norm_sales_amount])

Sales Qty = SUM(transactions[sales_qty])

Revenue Contribution % =
DIVIDE(
    [Revenue],
    CALCULATE(
        [Revenue],
        ALL(products),
        ALL(customers),
        ALL(markets)
    )
)
