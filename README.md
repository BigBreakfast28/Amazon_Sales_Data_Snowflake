# Amazon_Sales_Data_Snowflake
This project analyzes Amazon sales data using **Snowflake and SQL** to uncover key business insights related to revenue, product performance, and sales trends.

---

## 🎯 Business Objective

The goal of this project is to leverage data analytics to:
- Identify top-performing products  
- Analyze revenue trends over time  
- Understand sales distribution across categories  
- Support data-driven decision-making

## What-if Scenario Simulation
![Simulation](Amazon_Sales_Data/images/dashboard_12.png)

---

## 📂 Dataset Overview

The dataset contains transactional sales data from Amazon, including:

- Order Date  
- Product Name / Category  
- Units Sold  
- Revenue  
- Region / Market (if applicable)  

The data is structured to allow for time-based analysis, aggregation, and performance evaluation.

---

## ⚙️ Technologies Used

- **Snowflake** (cloud data warehouse)  
- **SQL** (data transformation and analysis)  
- **Snowsight Dashboard / Visualization** (optional)  

---

## 🧠 Key Analysis Performed

### 1. Sales Performance Analysis
- Aggregated total revenue by product  
- Identified top-selling and low-performing items  

### 2. Time Series Analysis
- Analyzed revenue trends over time  
- Identified seasonal patterns and fluctuations  

### 3. Product & Category Insights
- Evaluated sales distribution across product categories  
- Highlighted high-impact categories contributing to total revenue  

### 4. Revenue Optimization
- Ranked products by revenue contribution  
- Identified opportunities to improve product strategy  

---

## 📊 Sample Query

```sql
-- Top 10 products by revenue
SELECT 
    product_name,
    SUM(revenue) AS total_revenue
FROM amazon_sales
GROUP BY product_name
ORDER BY total_revenue DESC
LIMIT 10;
