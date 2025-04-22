# DATA-ANALYST-INTERNSHIP-Task-2
Data Visualization and Storytelling

# 🛒 Superstore Sales Data - Data Cleaning & Visualization Documentation

This README file documents the data preprocessing and visualization preparation steps applied to the `Sample - Superstore.csv` dataset as part of a Data Analyst Internship Task focused on **data storytelling with Power BI**.

---

## 📦 Dataset Overview

- **Filename**: `Sample - Superstore.csv`
- **Records**: 9,994
- **Columns**: 21
- **Purpose**: Analyze retail sales performance, customer behavior, product trends, and regional performance.

### 📊 Key Fields:
- **Sales, Profit, Discount, Quantity**
- **Product Info**: Category, Sub-Category, Product Name, Product ID
- **Customer Info**: Segment, State, City, Region
- **Order Info**: Order ID, Order Date, Ship Date, Ship Mode

---

## ✅ Data Preprocessing Steps

### 🔹 1. Column Standardization
- Renamed columns to be clean and consistent (e.g., `Order ID`, `Order Date`, `Customer Name`, `Product Category`, etc.).

### 🔹 2. Date Formatting
- Converted `Order Date` and `Ship Date` from `mm/dd/yyyy` to **`dd/mm/yyyy`** using Power BI Power Query Editor (`Using Locale` > English (United Kingdom)).

### 🔹 3. Data Types Correction
- Ensured appropriate data types:
  - `Order Date`, `Ship Date`: `Date/Time`
  - `Postal Code`: Converted to **string** to preserve ZIP codes like `01234`.
  - `Sales`, `Profit`, `Discount`: Float
  - `Quantity`: Integer
  - `Segment`, `Region`, `Category`: Text/Category

### 🔹 4. Duplicate Removal
- Removed exact duplicate records using `.drop_duplicates()` in Python.

### 🔹 5. Text Standardization
- Standardized all `object` columns to **Title Case**.
- Ensured:
  - `State` in **UPPERCASE**
  - Phone numbers formatted to: `+1-XXX-XXX-XXXX`

### 🔹 6. Missing Values
- Checked and verified minimal or no missing values.
- No major imputations were needed.

---

## 📊 Dashboard Design & Storytelling (Power BI)

### 🔸 KPIs Displayed:
- Total Sales
- Average Discount
- Average Profit Margin
- Total Orders

### 🔸 Interactive Filters (Slicers):
- Segment
- Region
- Category
- Order Date

### 🔸 Visual Elements:
| Visual Type | Purpose |
|-------------|---------|
| **Line Chart** | Sales trends over time |
| **Tree Map** | Sales by Category and Sub-Category |
| **Map / Bar** | Sales by Region and State |
| **Scatter Plot** | Discount vs Profit |
| **Stacked Bar** | Profit by Segment |
| **Data Table** | Top Products by Profit |

---

## 🎯 Outcome

- Data cleaned and structured for analytical modeling.
- Dashboard design reflects actionable insights:
  - Profitability by category
  - Discount impact
  - Customer segment contributions
  - Geographic sales trends

---

## 📌 Next Steps
- Add predictive forecasting to future dashboards.
- Integrate customer churn and CLTV metrics.
- Enhance visuals with custom tooltips and drill-down options.
