# 🍔 Swiggy Food Delivery Analytics

**End-to-End Data Pipeline using Microsoft Fabric, SQL, and Power BI**

---

## 📌 Project Overview

This project builds a complete data analytics solution for Swiggy — one of India's largest food delivery platforms. Raw order data is ingested, cleaned, modeled, and visualized to generate business insights on sales, restaurant performance, and customer behavior.

---

## 🏗️ Architecture
```
Raw CSV Files → Lakehouse (swiggy_lh) → Pipeline (lw_to_dw) → Data Warehouse (swiggy_wh) → Semantic Model (swiggy_pbi) → Power BI Report
```

---

## 🛠️ Technology Stack

| Layer | Tool |
|---|---|
| Data Storage | Microsoft Fabric Lakehouse |
| Data Pipeline | Microsoft Fabric Pipeline |
| Data Cleaning | SQL |
| Data Warehouse | Microsoft Fabric Warehouse |
| Semantic Layer | Power BI Semantic Model |
| Visualization | Power BI Report |

---

## 📊 Dashboard Highlights

![Dashboard](screenshots/dashboard.png)

| Metric | Value |
|---|---|
| Total Sales | ₹53.01M |
| Total Orders | 197.43K |
| Avg Order Value | ₹268.51 |
| Avg Rating | 4.34 |
| Rating Count | 5.59M |

### Visuals Included
- Monthly, Daily, and Weekly Sales Trends
- Top 5 Restaurants by Sales
- Top 15 States by Sales
- Veg vs Non-Veg Sales Breakdown
- Slicers: City, Food Type, Quarter, Restaurant

---

## 🗃️ Data Model (Star Schema)

**Fact Table**
- `fact_orders` — order_id, date_id, location_id, restaurant_id, food_id, price, rating, rating_count

**Dimension Tables**
- `dim_date` — date_id, order_date
- `dim_dish` — dish_id, category, dish_name
- `dim_location` — location_id, state, city, location
- `dim_restaurant` — restaurant_id, restaurant_name

---

## 🧹 Data Cleaning (SQL)

- Removed duplicate order records
- Handled NULL values in price and rating columns
- Validated referential integrity between fact and dimension tables
- Checked for negative price values
- Standardized date formats

---

## 📁 Repository Structure
```
swiggy-fabric-analytics/
├── README.md
├── data/
│   ├── fact_orders.csv
│   ├── dim_date.csv
│   ├── dim_dish.csv
│   ├── dim_location.csv
│   └── dim_restaurant.csv
├── screenshots/
│   ├── dashboard.png
│   └── workspace.png
└── docs/
    └── Business_Requirement.docx
```

---

## 👤 Author

**Syed Althamas**
Aspiring Data Analyst | Hyderabad, India
[GitHub](https://github.com/althamas-syed)# swiggy-fabric-analytics
End-to-end data analytics pipeline using Microsoft Fabric, SQL and Power BI
