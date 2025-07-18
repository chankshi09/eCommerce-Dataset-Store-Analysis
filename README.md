# 🛒 eCommerce Store Dashboard – SQL Project

This project analyzes a fictional eCommerce dataset using SQL and visualizes the insights using Power BI. It covers customer orders, demographics, channels, product categories, and geographic shipment details.

## 📁 Dataset Overview

The dataset includes detailed information about customer orders, such as:

| Column Name      | Description                                    |
| ---------------- | ---------------------------------------------- |
| Order ID         | Unique identifier for each order               |
| Cust ID          | Unique identifier for each customer            |
| Gender           | Gender of the customer (Men/Women/W)           |
| Age              | Age of the customer                            |
| Date             | Order date                                     |
| Status           | Delivery status (Delivered/Cancelled/Returned) |
| Channel          | Platform used (Amazon, Myntra, Flipkart, etc.) |
| SKU              | Product SKU code                               |
| Category         | Product category (Kurta, Set, Dress, etc.)     |
| Size             | Product size (S, M, L, XL, etc.)               |
| Qty              | Quantity purchased                             |
| Currency         | Transaction currency                           |
| Amount           | Order amount                                   |
| Ship-City        | Destination city                               |
| Ship-State       | Destination state                              |
| Ship-Postal-Code | Postal code of delivery                        |
| Ship-Country     | Country code                                   |
| B2B              | Order type (Business-to-Business or not)       |

---

## 📊 Dashboard Insights

### ✅ Order Status Distribution

* **92.25%** of orders are successfully **Delivered**
* Others include **Returned**, **Cancelled**, and **Refunded**

### 👩‍🦱 Gender vs Shopping

* **64.05%** of purchases are made by **Women**
* **35.95%** by **Men**

### 📦 Order Volume and Revenue

* Monthly breakdown of **Order Count vs Amount**
* Peak revenue months: **June–August**

### 🌍 Geographic Analysis

* **Top Shipping States**: Uttar Pradesh, Telangana, West Bengal
* **Top Cities**: Zirakpur, Gurugram, Bengaluru

### 🧒 Age Group Analysis

* Customers grouped as:

  * **Teenagers (13–19)**
  * **Adults (20–59)**
  * **Seniors (60+)**
* Adults contribute the majority of orders.

### 📦 Top Categories & Channels

* **Popular Product Categories**: Set, Kurta, Top, Western Dress
* **Top Channels**: Amazon, Myntra, Flipkart

### 🏢 B2B vs B2C

* **97.87%** of orders are **B2C**
* Only **2.13%** are B2B transactions

---

## 🛠 SQL Highlights

Some of the key SQL queries used in this analysis:

```sql
-- Total Orders
SELECT COUNT(*) AS Total_Orders FROM orders;

-- Orders by Gender
SELECT Gender, COUNT(*) AS Orders FROM orders GROUP BY Gender;

-- Revenue by State
SELECT ship_state, SUM(Amount) AS Revenue FROM orders GROUP BY ship_state ORDER BY Revenue DESC;

-- Monthly Order Trends
SELECT MONTH(Date) AS Month, COUNT(Order_ID) AS Total_Orders, SUM(Amount) AS Total_Amount
FROM orders
GROUP BY MONTH(Date);
```

---

## 📌 Tools Used

* **Database**: MySQL
* **Visualization**: Power BI
* **Language**: SQL
* **Platform**: GitHub

---

## 📷 Dashboard Preview

<img src="dashboard-image-link" alt="eCommerce Dashboard" width="800"/>

(Replace `"dashboard-image-link"` with your GitHub-hosted image)

---

## ✅ Conclusion

This project showcases how structured SQL queries and Power BI visuals can turn raw eCommerce data into actionable insights. It can be a great portfolio piece for data analysts or business intelligence professionals.

---

📬 Contact

Made by Chankshi Shrawankar 🔗 www.linkedin.com/in/chankshishrawankar | ✉️ chankshishrawankar@gmail.com

---

Would you like me to convert this into a Markdown `.md` file or upload-ready format for GitHub?
