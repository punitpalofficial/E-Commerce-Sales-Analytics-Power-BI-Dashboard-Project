# 🛒 E-Commerce Sales Analytics — Power BI Dashboard  
### **By Punit Pal**

![Power BI](https://img.shields.io/badge/PowerBI-Dashboard-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![Data Modeling](https://img.shields.io/badge/Star%20Schema-Modeling-blue?style=for-the-badge)
![DAX](https://img.shields.io/badge/DAX-Measures-yellow?style=for-the-badge)
![Project](https://img.shields.io/badge/End--to--End-Analytics-green?style=for-the-badge)

---

## 🔗 **Quick Navigation**
- [📌 Project Overview](#-project-overview)
- [📊 Dashboard Preview](#-dashboard-preview)
- [🧩 Dataset Structure](#-dataset-structure)
- [🏗️ Data Model (Star Schema)](#️-data-model-star-schema)
- [📈 Key KPIs (DAX Measures)](#-key-kpis-dax-measures)
- [🔍 Major Insights](#-major-insights)
- [🛠 Tools Used](#-tools-used)
- [📥 How to Use](#-how-to-use)
- [🎯 Business Outcomes](#-business-outcomes)
- [🙌 Credits](#-credits)
- [⭐ About Me](#-about-me)

---

# 📌 **Project Overview**

This **Power BI E-Commerce Sales Dashboard** provides a complete analytical view of business performance, analyzing:

- Revenue trends  
- Top-performing products  
- Category-wise & state-wise performance  
- Customer characteristics  
- Order volume and cancellations  
- Lost revenue impact  
- Quarterly time-series patterns  

This dashboard enables powerful business decisions based on real customer & sales data.

---

# 📊 **Dashboard Preview**

<p align="center">
  <img src="Ecom_Express_Sales_Dashboard" width="800">
</p>


---

# 🧩 **Dataset Structure**

<details>
<summary><strong>📄 customers Table</strong></summary>

| Column | Description |
|--------|-------------|
| CustomerID | Unique customer reference |
| Full_Name | Customer's name |
| City | Customer city |
| State | Residential state |
| Phone Brand | Xiaomi, Samsung, Apple, etc. |
| OS | Android / iOS |

</details>

<details>
<summary><strong>📄 products Table</strong></summary>

| Column | Description |
|--------|-------------|
| ProductID | Unique product reference |
| Product Name | Product title |
| Category | Laptop, Mobile, Accessories, etc. |
| Price | Item price |
| Rating | Customer rating |

</details>

<details>
<summary><strong>📄 orders Table</strong></summary>

| Column | Description |
|--------|-------------|
| OrderID | Unique order ID |
| Date and time of purchase | Timestamp |
| Delivery Status | Delivered / Cancelled |
| Delivery time | Days to deliver |
| Quantity | Units ordered |
| CustomerID | Customer reference |
| ProductID | Product reference |

</details>

---

# 🏗️ **Data Model (Star Schema)**

> *(Add your model screenshot here)*


✔ Fact Table: **orders**  
✔ Dimension Tables: **customers**, **products**  
✔ KPI Table: **measures**  

---

# 📈 **Key KPIs (DAX Measures)**

### 💰 **Total Revenue**
DAX
Revenue =
SUMX(orders, orders[Quantity] * RELATED(products[Price]))

### 📦 **Total Orders**
Total Orders = COUNTROWS(orders)
### 📉  **Cancellation Rate**
Cancellation Rate =
VAR TotalOrders = COUNTROWS(orders)
VAR Cancelled =
CALCULATE(COUNTROWS(orders),
orders[Delivery Status] = "Cancelled")
RETURN DIVIDE(Cancelled, TotalOrders)

### 💸  **Lost Revenue from Cancellations**
Lost Revenue Cancellation =
CALCULATE([Revenue], orders[Delivery Status] = "Cancelled")

### 📒 **Average Order Value**
AOV = DIVIDE([Revenue], DISTINCTCOUNT(orders[OrderID]))


# 🔍 **Major Insights**

### 🔹 **1. Revenue by Category**

* Laptops generate the highest revenue
* Mobile & Headphones categories follow
* Minimal revenue from cables & mouse accessories

### 🔹 **2. Best Performing Products**

Top-selling items include:

* MacBook Air
* OnePlus 9
* HP Pavilion
* Sony Headphones
* Samsung Galaxy Series

### 🔹 **3. Top Revenue States**

* Maharashtra
* Gujarat
* Rajasthan
* West Bengal
* Karnataka

### 🔹 **4. Quarterly Trends**

* **Q3 shows highest spike** (festive season)
* Q4 shows decline

### 🔹 **5. Cancellation Impact**

* **29.72% orders cancelled**
* **₹525.42M lost revenue**

---

# 🛠 **Tools Used**

| Tool                 | Purpose                   |
| -------------------- | ------------------------- |
| **Power BI Desktop** | Dashboard & modeling      |
| **Power Query**      | Cleaning & transformation |
| **DAX**              | Calculations & KPIs       |
| **Excel**            | Initial dataset           |
| **Star Schema**      | Data modeling             |

---

# 📥 **How to Use**

1. Download the PBIX file
2. Open with **Power BI Desktop**
3. Explore slicers, filters & insights
4. Use the dashboard for strategic decisions

---

# 🎯 **Business Outcomes**

This dashboard helps businesses:

* Identify profitable products
* Reduce cancellation losses
* Target high-value customer regions
* Understand seasonal revenue patterns
* Improve sales & marketing strategies
* Optimize stock & delivery operations

---

# 🙌 **Credits**

Inspired & guided by:
**WsCube Tech** & **Ayushi Jain**
Thank you for amazing learning content! 🙏

---

# ⭐ **About Me — Punit Pal**

**Data Analyst | SQL | Power BI | Excel | Visualization**
Passionate about turning raw data into powerful business insights.

📩 *Open to Data Analyst Internships & Opportunities*  

For collaborations or questions:  
🔹 **LinkedIn:** https://www.linkedin.com/in/punit-pal/  
🔹 **GitHub:** https://github.com/punitpalofficial  
🔹 **Email:** punitpalofficial@gmail.com

---

# 🚀 **If you like this project, don't forget to ⭐ the repository!**

---
# ⭐ Support

If you found this project helpful, please ⭐ the repository.  
Your support motivates me to create more analytics projects!

---
