

---

# 🍕 Pizza Sales Analytics Dashboard

## 🎯 Project Overview

This **interactive Power BI dashboard** presents insights into **Pizza Sales** using real sales data. The dashboard leverages **DAX** for calculating meaningful sales metrics, applying time intelligence, analyzing trends, and presenting key business insights. The objective is to provide a visual understanding of **pizza sales trends, performance** by category, **customer ordering patterns**, and **business growth** over time.

---

## 🔗 **Demo**

![Demo](pizza-sales.gif)

---

## 📊 Key Features

### 1. **Sales Overview**

* Total sales, total orders, total quantity of pizzas sold, and average order value.
* Year-over-Year (YoY) and Month-over-Month (MoM) sales growth.
* Dynamic time slicers for interactive analysis by year, month, and quarter.

### 2. **Pizza Performance**

* Sales by **Pizza Category** and **Pizza Type**.
* **Top 5 Best-Selling Pizzas** by quantity and revenue.
* **Treemaps** to visualize the performance breakdown by pizza size and category.

### 3. **Time Intelligence**

* Trend analysis of pizza sales **monthly** and **weekly**.
* MTD (Month-to-Date), QTD (Quarter-to-Date), and YTD (Year-to-Date) calculations.
* Sales comparison across different time periods (Last Month, Last Year).

### 4. **Customer Insights**

* Order trends by **Day of Week** and **Time of Day**.
* **Quantity per order** and **Average Order Value** by month.

---

## 📁 Provided Dataset Files

Download the **pizza_sales dataset** which contains the following CSV files:

* **orders.csv**

  * order_id
  * date
  * time
* **order_details.csv**

  * order_details_id
  * order_id
  * pizza_id
  * quantity
* **pizzas.csv**

  * pizza_id
  * pizza_type_id
  * size
  * price
* **pizza_types.csv**

  * pizza_type_id
  * name
  * category
  * ingredients

---

## 🧠 Project Learning Outcomes & DAX Focus

In this project, students will:

* Build a **star schema model** in Power BI.
* Use **DAX** to:

  * Create **calculated columns** for derived insights (e.g., Total Price, Day of Week, Month, etc.).
  * Develop **measures** to calculate KPIs (e.g., Total Sales, Avg. Order Value, Sales by Category).
  * Apply **time intelligence** functions like **SAMEPERIODLASTYEAR**, **PARALLELPERIOD** to track growth.
  * Use functions like **CALCULATE**, **FILTER**, **RANKX**, **SWITCH**, **IF** to manage complex data models and create custom reports.

---

## 🔨 Tasks Breakdown

### 1. **Data Modeling**

* Import and clean CSV files in Power BI.
* Create relationships:

  * **orders** ↔ **order_details** via `order_id`.
  * **order_details** ↔ **pizzas** via `pizza_id`.
  * **pizzas** ↔ **pizza_types** via `pizza_type_id`.
* Create a **Calendar Table** for time-based analysis.

### 2. **DAX Calculations**

#### Calculated Columns:

* **Total Price**: `quantity * price` from `order_details`.
* **Day of Week**, **Month**, **Year** extracted from `orders[date]`.
* **Pizza Size Label**: E.g., "Small", "Medium", etc.

#### Measures:

| Measure                       | Description                                   |
| ----------------------------- | --------------------------------------------- |
| **Total Sales**               | Sum of `total price`.                         |
| **Total Pizzas Sold**         | Sum of `quantity`.                            |
| **Avg. Order Value**          | `Total Sales / No. of Orders`.                |
| **No. of Orders**             | `DISTINCTCOUNT(order_id)`.                    |
| **Sales by Category**         | Aggregated by `pizza_types[category]`.        |
| **Sales by Pizza Size**       | Breakdown by pizza size.                      |
| **Top 5 Best-Selling Pizzas** | Use **RANKX** for rankings.                   |
| **YoY Sales Growth**          | Calculate growth using **time intelligence**. |

### 3. **Time Intelligence**

* **MTD**, **QTD**, **YTD Sales**.
* **Last Year’s Sales** comparison using `SAMEPERIODLASTYEAR`, `PARALLELPERIOD`.
* **MoM** and **YoY comparison** visuals.

### 4. **Dashboard Visuals**

* **Summary Page**: Total sales, orders, quantity, and Avg. order value with dynamic date slicers.
* **Pizza Performance**: Sales by category and pizza type, and top 5 best-sellers.
* **Trend Analysis**: Line charts to display sales over time.
* **Customer Insights** (Optional): Visualize orders by time of day and day of the week.

---

## 🔧 Features and Functionalities

* **Interactive filters** for dynamic analysis (select by month, quarter, region, or pizza type).
* **Visual drill-downs** to explore detailed data for sales, orders, and pizza categories.
* **Trendlines** and **KPIs** for tracking sales performance over time.
* **Ranking features** to display the top-selling pizzas and categories.

---

## 👨‍💻 Developer

**Abu Usama**
Data Analyst | BI Developer | Dashboard Specialist

🌍 Connect with me:
[![GitHub](https://img.icons8.com/fluent/48/000000/github.png)](https://github.com/UsamaMunawarr)[![LinkedIn](https://img.icons8.com/color/48/000000/linkedin.png)](https://www.linkedin.com/in/abu--usama)[![YouTube](https://img.icons8.com/?size=50\&id=19318\&format=png)](https://www.youtube.com/@CodeBaseStats)[![Twitter](https://img.icons8.com/color/48/000000/twitter.png)](https://twitter.com/Usama__Munawar)[![Facebook](https://img.icons8.com/color/48/000000/facebook-new.png)](https://www.facebook.com/profile.php?id=100005320726463)

---

## 📝 License

This project is licensed under the **MIT License**.


