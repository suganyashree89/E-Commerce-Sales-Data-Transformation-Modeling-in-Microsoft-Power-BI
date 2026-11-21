# E-Commerce Sales Data Transformation & Modeling in Microsoft Power BI

## 📌 Project Overview

This project covers the end-to-end import, cleaning, transformation, merging, aggregation, and data modeling of **e-commerce sales datasets** in **Microsoft Power BI** (`Data Transformation & Data Modeling Assignment-1`). Using **Power Query**, raw e-commerce order records, order details, and monthly sales targets are processed into clean, analysis-ready tables connected via active relationships to drive interactive sales and target performance reporting.

## 🎯 Objectives

* **Raw Data Ingestion:** Import raw e-commerce datasets (`Raw_List of Orders`, `Raw_Order Details`, and `Raw_Sales target`) into Power BI Desktop.
* **ETL & Data Cleansing (Power Query):** Create dedicated staging/processing queries (`Processing_List of Orders`, `Processing_Order Details`, `Processing_Sales target`) to standardize data types, remove blanks/duplicates, and format dates and currency values.
* **Merging & Aggregation:** Combine order headers with line-item details (`Order Data`) and build summarized aggregation tables (by Category, Sub-Category, Order ID, and Month) for streamlined reporting.
* **Data Modeling & Active Relationships:** Establish active relationships across order, detail, and target tables to support accurate cross-filtering and KPI tracking.

## 🛠️ Tools & Technologies

* **Microsoft Power BI Desktop**
* **Power Query (M Language)** – Data import, cleaning, query referencing, merging, and Group By aggregations
* **Power BI Model & Report View** – Relational modeling and interactive dashboarding

## 🗂️ Data Architecture & Queries

Based on the Power BI data pane structure, the workflow organizes queries into three clear stages:

### 1. Raw Layer (Source Tables)
* `Raw_List of Orders`: Source order-level metadata (Order ID, Order Date, Customer details, location).
* `Raw_Order Details`: Source line-item transaction data (Order ID, Amount, Profit, Quantity, Category, Sub-Category).
* `Raw_Sales target`: Source monthly sales targets by product category.

### 2. Processing & Reference Layer (Power Query Transformations)
* `Processing_List of Orders` & `reference list order`: Cleaned and standardized order header records.
* `Processing_Order Details`: Cleansed line-item transactions with enforced numeric and text formatting.
* `Processing_Sales target`: Standardized target dates and target amounts per category.
* `Order Data`: Merged master dataset combining order attributes and transaction details.

### 3. Aggregated Summary Tables
* `Total amount` & `Total Amount by sub-category`: Pre-aggregated sales totals across product sub-categories.
* `Total Of Target` & `Total Target by month`: Aggregated target benchmarks over time (2018–2019).
* `Average profit by category`: Category-level profitability summary.
* `count of category` & `count of order_id`: Order and category volume metrics.

## 📊 Key Dashboard Insights & Visuals

The Power BI report highlights core e-commerce KPIs and category breakdowns:
<img width="749" height="438" alt="image" src="https://github.com/user-attachments/assets/502bbed8-3145-4644-ab3c-7f42b88a6e2d" />

* **Headline KPI Cards:**
  * **Total Sales Amount:** `431.50K`
  * **Total Sales Target:** `435.90K`
* **Sales by Sub-Category (Bar Chart):** Top-performing sub-categories include **Printers (`58K`)**, **Bookcases (`57K`)**, **Saree (`54K`)**, **Phones (`46K`)**, and **Electronic Games (`39K`)**, down to **Shirt (`8K`)** and **T-shirt (`7K`)**.
* **Order Volume by Category (Bar Chart):** **Clothing** leads significantly in item/order count, followed by **Electronics** and **Furniture**.
* **Target Distribution by Year (Pie Chart):** **2018** accounts for `305K` (`69.97%`) of the total target, while **2019** accounts for `130.9K` (`30.03%`).
* **Target Allocation by Category (Ribbon/Area Chart):** **Clothing (`174K`)**, **Furniture (`133K`)**, and **Electronics (`129K`)**.

## 📂 Repository Structure

```text
├── data/                   # Raw e-commerce CSV/Excel source files (List of Orders, Order Details, Sales Target)
├── powerbi/                # Data Transformation & Data Modeling Assignment-1.pbix
├── screenshots/            # Dashboard and Data Model screenshots
└── README.md               # Project documentation
```

## 🚀 How to Use

1. **Clone the repository:**
   ```bash
   git clone https://github.com/suganyashree89/ecommerce-sales-powerbi.git
   ```
2. **Open the Power BI File:**
   * Launch **Microsoft Power BI Desktop**.
   * Open `Data Transformation & Data Modeling Assignment-1.pbix` from the `powerbi/` folder.
3. **Reconnect Data Sources:**
   * Navigate to **Home > Transform data > Data source settings** to update file paths to your local `data/` directory, then select **Refresh**.
4. **Explore Queries & Model:**
   * Open **Transform data (Power Query Editor)** to inspect the `Raw_`, `Processing_`, and aggregated queries.
   * Switch to **Model View** to review active table relationships.

## ✅ Conclusion

Through systematic data import, cleaning, transformation, merging, aggregation, and modeling in **Microsoft Power BI**, the raw e-commerce datasets (`Raw_List of Orders`, `Raw_Order Details`, and `Raw_Sales target`) are converted into a structured, reliable, and analysis-ready reporting foundation.

* **Reliable Data Preparation:** Separating raw inputs from `Processing_` queries in Power Query ensures clean formatting, accurate data types, and traceable transformations.
* **Unified Analytical View:** Merging order headers with line-item details (`Order Data`) and generating targeted aggregations (`Total amount`, `Total Of Target`, `Average profit by category`) delivers clear visibility across categories and sub-categories.
* **Scalable Reporting Model:** Establishing active relationships enables accurate cross-filtering and clean tracking of actual sales (`431.50K`) against targets (`435.90K`), ensuring future e-commerce data updates integrate seamlessly.
