<div align="center">

# -- ! Myntra Sales & Product Analysis — Power BI Dashboard ! --
### *Interactive Orders, Revenue, Brand & Inventory Analysis using Power BI*

[![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)](https://powerbi.microsoft.com/)
[![Dataset](https://img.shields.io/badge/Data-Orders%20%2B%20Product%20Catalog-4472C4?style=for-the-badge)](#-overview)
[![Analysis](https://img.shields.io/badge/Analysis-Sales%20%26%20Product-F39C12?style=for-the-badge)](#-part-c--kpi-analysis)
[![Dashboard](https://img.shields.io/badge/Dashboard-2%20Pages-008C95?style=for-the-badge)](#-part-d--interactive-dashboard)

<br/>

> *"Turn raw Myntra order and product data into clear, interactive insights with Power BI."*

</div>

---

## 📋 Table of Contents

- [📌 Overview](#-overview)
- [🎯 Problem Statement](#-problem-statement)
- [✨ Key Features](#-key-features)
- [🏗️ Project Structure](#️-project-structure)
- [🔄 Project Workflow](#-project-workflow)
- [🧹 Part A — Dataset Import](#-part-a--dataset-import)
- [🧽 Part B — Data Cleaning & Modeling](#-part-b--data-cleaning--modeling)
- [📊 Part C — KPI Analysis](#-part-c--kpi-analysis)
- [📈 Part D — Interactive Dashboard](#-part-d--interactive-dashboard)
- [🛠️ Tech Stack](#️-tech-stack)
- [📈 Results & Insights](#-results--insights)
- [🏆 Advantages](#-advantages)
- [📄 License](#-license)
- [👤 Author](#-author)
- [🙏 Acknowledgements](#-acknowledgements)

---

## 📌 Overview

The **Myntra Sales & Product Analysis — Power BI Dashboard** is a two-page Power BI report built on Myntra-style e-commerce data: an **orders table** and a **product catalog** of **2,500 products**, with about **12K orders**. The report is stamped **Data as of 30-Apr-2025**.

The report takes the data through a complete analysis workflow:

- Import the orders and product catalog into Power BI
- Clean the data and build a **Calendar** table and an unpivoted **Inventory** table
- Build KPI cards for **Total Orders, Total Revenue and Total Products**
- Create visuals by **Category, Brand, City Tier, Size and Order Status**
- Add interactive **Brand, Category and City Tier** slicers
- Add a **Top 10 Products by Revenue** table

### 📁 Dataset Information

| Item | Details |
|------|---------|
| Orders table | `myntra_Orders_Master` |
| Product table | `myntra_product_catalog` |
| Date table | `Calendar` |
| Inventory table | `Inventory_Unpivot` (size-wise stock) |
| Measures table | `measure_tables` |
| Total Products | **2,500** |
| Total Orders | **≈ 12K** |
| Main Dimensions | Brand, Category, Product, City Tier, Size, Order Status, Date |

---

## 🎯 Problem Statement

> **Objective:** Transform Myntra order and product data into an interactive Power BI dashboard that shows which brands and categories drive revenue, how cities and order statuses are split, and how inventory is spread across sizes.

| 📂 Project Area | 📄 Type | 🔍 Description |
|----------------|---------|----------------|
| Raw Data | Source Data | Orders and product catalog imported into Power BI |
| Data Model | Data Preparation | Calendar table, unpivoted inventory, Brand / Category grouping |
| KPI Cards | Measures | Total Orders, Total Revenue, Total Products, Total Inventory |
| Charts | Visualization | Orders by Category / Brand / City Tier, Revenue by Brand and City Tier |
| Slicers | Interactivity | Brand, Category and City Tier filters |
| Detail Table | Drill-down | Top 10 products with brand, category, orders and revenue |

---

## ✨ Key Features

| Feature | Description |
|--------|-------------|
| 📥 **Data Import** | Orders and product catalog loaded directly into Power BI |
| 🧹 **Data Preparation** | Calendar table, inventory unpivot, Brand Group and Category Group columns |
| 📌 **KPI Cards** | Total Orders and Total Revenue with a trend sparkline |
| 📉 **Month-over-Month Change** | Red / green arrow showing change vs the previous month |
| 🍩 **Product Distribution** | Donut chart of products by category |
| 📦 **Size-wise Inventory** | Column chart of stock by size (M, L, S, XS, XL) |
| 🏷️ **Brand Performance** | Revenue by brand in ₹ Cr |
| 🏙️ **City Tier Analysis** | Revenue and orders split across Tier 1, Tier 2 and Tier 3 |
| 🚚 **Order Status Distribution** | Delivered, Returned, Shipped and Cancelled |
| 🎛️ **Interactive Slicers** | Brand, Category and City Tier checkboxes update the visuals |
| 📋 **Top 10 Products Table** | Product-level revenue ranking |
| 🔄 **Live Cross-Filtering** | Click any visual to filter the rest of the page |

---

## 🏗️ Project Structure

```text
📦 PowerBI-MyntraDashboard/
│
├── 📄 Myntra_Dashboard.pbix       ← Main Power BI report
├── 📄 README.md                   ← Project documentation
│
└── 📁 assets/
    ├── 🖼️ 01_product_analysis.png
    └── 🖼️ 02_sales_overview.png
```

### 📚 Report Map

| Page | Purpose |
|------|---------|
| **Product Analysis** | Product mix, size-wise inventory, brand and city-tier revenue, top products, order status |
| **Sales Overview** | KPI cards, slicers, orders by city tier, category and brand |

### 🖼️ Product Analysis Preview

![Product Analysis](assets/01_product_analysis.png)

---

## 🔄 Project Workflow

```text
Project Start
      │
      ▼
┌────────────────────────────────────┐
│  Step 1 — Import Data             │
│  Orders + Product Catalog         │
└───────────────┬────────────────────┘
                │
                ▼
┌────────────────────────────────────┐
│  Step 2 — Clean & Model Data      │
│  Calendar + Inventory Unpivot     │
└───────────────┬────────────────────┘
                │
                ▼
┌────────────────────────────────────┐
│  Step 3 — Create DAX Measures     │
│  Orders / Revenue / MoM change    │
└───────────────┬────────────────────┘
                │
                ▼
┌────────────────────────────────────┐
│  Step 4 — Build Visuals           │
│  Donut, bar, column, line, table  │
└───────────────┬────────────────────┘
                │
                ▼
┌────────────────────────────────────┐
│  Step 5 — Add Slicers & Format    │
│  Brand + Category + City Tier     │
└───────────────┬────────────────────┘
                │
                ▼
┌────────────────────────────────────┐
│  Step 6 — Publish / Share         │
│  Final interactive dashboard      │
└────────────────────────────────────┘
```

---

## 🧹 Part A — Dataset Import

### 📝 1. Source Data

The project uses two main tables:

- **`myntra_Orders_Master`** — order-level data (order status, city tier, brand, category, date, revenue)
- **`myntra_product_catalog`** — product-level data (product name, brand, category, size, inventory)

### 📌 2. How to Load

1. Open Power BI Desktop
2. **Home → Get Data → Text/CSV** (or Excel)
3. Select the orders file, then the product catalog file
4. Click **Transform Data** to check types, then **Close & Apply**

---

## 🧽 Part B — Data Cleaning & Modeling

### 🔍 3. Preparation Steps

- Checked column data types (dates, whole numbers, decimals, text)
- Created a **Calendar** table and linked it to the order date
- Created **`Inventory_Unpivot`** to turn size columns into rows for size-wise inventory
- Created **Brand Group** and **Category Group** so smaller brands and categories roll up into "Others"
- Placed all DAX measures in a separate **`measure_tables`** table

### 📊 4. Measures Used

| Measure | Purpose |
|--------|---------|
| **Total Orders** | Count of orders |
| **Total Revenue / Revenue Cr** | Revenue, shown in ₹ and in ₹ Crore |
| **Total Products** | Count of products in the catalog |
| **Total Inventory** | Stock across sizes |
| **Orders MoM Text / Color** | Month-over-month change text and red / green colour for the orders card |
| **Revenue MoM Text / Color** | Month-over-month change text and red / green colour for the revenue card |

---

## 📊 Part C — KPI Analysis

The dashboard displays headline KPI cards that respond to the slicers:

| KPI | Description |
|-----|-------------|
| **Total Orders** | Orders for the current selection (with sparkline and change vs Mar-2025) |
| **Total Revenue** | Revenue in ₹ Cr (with sparkline and change vs Mar-2025) |
| **Total Products** | Number of products in the catalog |

### 📌 Values Shown on the Dashboard

| Metric | Value |
|-------|-------|
| Total Products | 2,500 |
| Total Orders (all) | ≈ 12K |
| Total Orders (Sales Overview card) | 5,858 · ▼ 5.1% vs Mar-2025 |
| Total Revenue (Sales Overview card) | ₹ 3.75 Cr · ▼ 3.5% vs Mar-2025 |
| Total Revenue (Top 10 table total) | ₹ 17,34,823 |

> The Sales Overview cards show the latest month with a comparison against Mar-2025, so they are lower than the all-time totals.

---

## 📈 Part D — Interactive Dashboard

### 🎛️ Dashboard Filters

- **Brand** — Adidas, Campus, H&M, HRX, Levi's, Nike and more
- **Category** — Dresses, Face Wash, Heels, Jeans, Kids Wear, Lipstick, Perfume and more
- **City Tier** — Tier 1, Tier 2, Tier 3

Selecting any checkbox updates the KPI cards and charts on the page.

### 📊 Visuals

| Visual | What it shows |
|-------|---------------|
| **Product Distribution** | Share of products by category (Others, Kids Wear, School Shoes, Face Wash, Lipstick) |
| **Size-wise Inventory** | Inventory by size: M, L, S, XS, XL |
| **Brand Performance (Revenue)** | Revenue by brand: Puma, Nike, Zara, H&M, Levi's, Adidas |
| **City Tier Analysis (Revenue)** | Revenue by Tier 2, Tier 1, Tier 3 |
| **Top 10 Products by Revenue** | Product, brand, category, total orders and total revenue |
| **Order Status Distribution** | Delivered, Returned, Shipped, Cancelled |
| **Orders by City Tier** | Order share across Tier 1, 2 and 3 |
| **Orders by Category** | Kids Wear, School Shoes, Face Wash, Lipstick, Perfume, Jeans |
| **Orders by Brand** | Order counts by brand |

### 🖼️ Sales Overview Preview

![Sales Overview](assets/02_sales_overview.png)

---

## 🛠️ Tech Stack

| Tool / Feature | Purpose |
|----------------|---------|
| 📊 **Power BI Desktop** | Report and dashboard creation |
| 📥 **Orders & Catalog Data** | Source data |
| 🧹 **Power Query** | Data cleaning, unpivot and type conversion |
| 📐 **DAX Measures** | Orders, revenue and month-over-month calculations |
| 📈 **Donut, Bar, Column & Line Charts** | Distribution and comparison |
| 🎛️ **Slicers** | Brand, Category and City Tier filters |
| 📋 **Table Visual** | Top 10 products by revenue |
| 🎨 **Formatting & Icons** | Dashboard design, Myntra branding |

---

## 📈 Results & Insights

- ✅ **2,500 products** and **≈ 12K orders** loaded and modeled in Power BI
- 📌 **KPI cards** show orders and revenue with a month-over-month change
- 🏷️ **Brands outside the top names** ("Others") contribute the largest revenue share, ahead of Puma, Nike and Zara
- 🏙️ **Tier 2 cities** lead in revenue, followed by Tier 1 and then Tier 3
- 🚚 **Order status** is split almost evenly, about 25% each across Delivered, Returned, Shipped and Cancelled
- 📦 **Size M** has the most inventory, and XS and XL the least
- 📋 **Top 10 table** helps trace the best-selling individual products

---

## 🏆 Advantages

| Advantage | Detail |
|-----------|--------|
| 🎓 **Beginner Friendly** | Shows a complete Power BI workflow from raw data to dashboard |
| 🎛️ **Interactive** | Brand, Category and City Tier slicers filter the visuals |
| 📊 **Visual** | KPI cards and charts make insights quick to read |
| 🔍 **Detailed** | Product-level table allows deeper investigation |
| 🔄 **Reusable** | Works with any e-commerce style orders and catalog data |
| 📚 **Portfolio Ready** | Clean structure with report and screenshots |

---

## 📄 License

This project is provided for **educational and portfolio purposes**.

You may adapt the report and documentation for your own learning or portfolio use, while keeping appropriate attribution for any source material you reuse. Myntra name and logo belong to their respective owner.

---

Video Link Here (https://drive.google.com/file/d/1SBf19sQnmdN9dnOzbrD0frVs1o1kuxcM/view?usp=sharing)

## 👤 Author

<div align="center">

### Myntra Sales & Product Analysis — Power BI Dashboard

> *"From raw rows to meaningful insights — one measure, one visual and one dashboard at a time."*

**👩‍💻 Author:** Yashvi Jasani  
**🎓 Project Type:** Power BI Data Analysis & Dashboard  
**📊 Focus:** Sales Performance, Product & Inventory Analysis, Visualization  
**🛠️ Skills:** Power BI · Power Query · DAX · Data Cleaning · KPI Measures · Slicers · Dashboard Design

</div>

---

## 🙏 Acknowledgements

This project was developed using Myntra-style orders and product catalog data and Power BI Desktop.

Key Power BI concepts demonstrated in the project include:

- Data import and cleaning
- Calendar table and unpivot
- DAX measures and month-over-month change
- KPI cards with sparklines
- Donut, bar and column charts
- Slicers and table visuals
- Dashboard layout and formatting

---

<div align="center">

---

*Made with ❤️ and 📊 — Last updated: 2 November, 2026*

</div>
