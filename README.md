# Coffee Sales Performance Dashboard

![Made with Excel](https://img.shields.io/badge/Made%20with-Excel-217346?logo=microsoft-excel&logoColor=white&style=flat)
![Power Query](https://img.shields.io/badge/Power%20Query-Data%20Transform-0078d4?logo=microsoft&logoColor=white&style=flat)
![Data Visualization](https://img.shields.io/badge/Data-Visualization-orange?style=flat)
![Interactive Dashboard](https://img.shields.io/badge/Interactive-Dashboard-blueviolet?style=flat)

## Overview

The **Coffee Sales Performance Dashboard** is an Excel-based interactive tool that provides a comprehensive overview of sales performance across coffee products, customer segments, and countries. This project demonstrates a complete workflow — from raw data preparation and transformation using Power Query to dynamic reporting with PivotTables and visual storytelling. The dashboard offers actionable insights into trends, product performance, key customers, and geographic distribution to support strategic decisions in a coffee retail business.

---

## Project Objectives

- Analyze overall coffee sales trends over time (monthly and yearly)
- Compare sales across different coffee types and roast categories  
- Identify the top 5 customers based on total sales  
- Evaluate geographic performance by country and product  
- Enable interactive data filtering using slicers for Coffee Type and Year  
- Present insights in a clean, user-friendly dashboard layout  

---

## Dataset

Dataset used for portfolio and demonstration purposes. Originally sourced from a publicly available dataset.

- <a href="https://github.com/Arianne-R/coffee-sales-performance-dashboard/blob/main/coffee_sales_raw_data.xlsx">coffee_sales_raw_data
- <a href="https://github.com/Arianne-R/coffee-sales-performance-dashboard/blob/main/coffee_sales_performance_dashboard.xlsx">coffee_sales_performance_dashboard
- <a href="https://github.com/Arianne-R/coffee-sales-performance-dashboard/blob/main/dashboard_preview.JPG">dashboard_preview

---

## Data Preparation

### Table Conversion

- Converted raw data in the `orders`, `customers`, and `products` worksheets into structured Excel Tables  
- Renamed the tables: `Orders`, `Customers`, and `Products` for consistency and ease of use  

### Power Query Transformations

- Imported all three tables into Power Query for centralized data processing  
- Merged `Orders` with `Customers` using **Customer ID** (Left Join to preserve all sales orders)  
- Merged the resulting table with `Products` using **Product ID** (Left Join to preserve all sales orders)   
- Performed data modeling by merging related tables to create a unified dataset for analysis
- Expanded and renamed key columns (e.g., `Customer Name.1` → `Customer Name`)  
- Removed duplicate or unnecessary columns created during merges to keep the dataset clean and easy to work with
- Standardized and replaced values in:  
  - **Coffee Type:**  
    - `Rob` → `Robusta`  
    - `Ara` → `Arabica`  
    - `Exc` → `Excelsa`  
    - `Lib` → `Liberica`  
  - **Roast Type:**  
    - `D` → `Dark`  
    - `L` → `Light`  
    - `M` → `Medium`    
- Removed any pre-existing `Sales` column and added a new calculated column:  
  - `Sales = [Unit Price] * [Quantity]`  
- Adjusted data types for accuracy:
  - `Order Date` → Date (Locale: English - United States)  
  - `Sales` and `Unit Price` → Currency  

### Output

- Loaded the cleaned, transformed data into a new worksheet named `Transformed Orders` for reporting and analysis  

---

## Key Dashboard Features

**1. Sales Trend Over Time**  
- Total sales aggregated by month and year
- Visualized with a **line chart**  to identify seasonal sales patterns and overall growth trends

**2. Sales by Coffee Type**  
- Breaks down sales performance by coffee type  
- Shown as a **clustered column chart**  
- Highlights Excelsa as the highest-selling coffee type

**3. Sales by Country and Coffee Type**  
- Compares regional performance  
- Visualized with a **stacked column chart**

**4. Top 5 Customers by Sales**  
- Displays the top 5 customers based on sales volume  
- Shown as a **clustered bar chart**  
- Filtered using Top-N logic to show only top 5 customers
- Highlights the top customer as the highest-selling within the top 5

**5. Interactive Filtering with Slicers**  
- **Year Slicer** – Filters charts based on the year of sale (grouped from `Order Date`)  
- **Coffee Type Slicer** – Filters multiple charts based on coffee type  

**6. Clean, Interactive Layout**  
- All visuals are organized in the `Dashboard` worksheet  

**7. Embedded Insights**  
- Key findings are summarized in text boxes within each worksheet to enhance clarity and decision-making

**8. Slicer-to-Pivot Connections**  
- **Coffee Type Slicer** controls:  
  - Sales by Coffee Type  
  - Sales by Country and Coffee Type  
  - Top 5 Customers by Sales 

- **Year Slicer** controls:  
  - Sales by Country and Coffee Type  
  - Top 5 Customers by Sales 

> **Note:** The Sales Trend Over Time chart (Pivot 1) is intentionally not connected to any slicers to preserve a full historical view.  
> The embedded insights are based on the full dataset. If slicers are used, charts will reflect filtered data — but written insights will **not** dynamically adjust.

---

## How to Use

1. **Open** ` coffee_sales_performance_dashboard.xlsx` in Microsoft Excel (desktop version recommended)  
2. **Go to** the `Dashboard` worksheet  
3. **Use** the slicers to filter data by Coffee Type or Year  
4. **Hover** over charts for detailed tooltips  
5. **Explore** underlying PivotTables in the following sheets:
   - `Sales_Trend`  
   - `CoffeeType_Sales`   
   - `Country_Sales`
   - `Top5_Customers`   

---

## Tools & Skills Demonstrated

**Data Preparation & Transformation (Power Query):**  
- Table conversion and naming  
- Data merging, integration, and modeling
- Standardization and cleaning  
- Custom calculated fields  

**Data Analysis (Excel):**  
- Grouped PivotTables  
- Aggregation and Top-N filtering  
- Monthly and categorical breakdowns  

**Visualization & Interactivity:**  
- Line, column, bar, and stacked charts  
- Use of slicers for dynamic filtering  
- Professional layout and dashboard design  

**Business Insight & Storytelling:**  
- Uncovers product, customer, and regional performance patterns  
- Supports data-driven decisions for sales strategy  
- Simplifies complex data into actionable visuals  

---

## Dashboard Preview

![dashboard_preview](https://github.com/user-attachments/assets/11f3cac0-d8d1-4f84-8405-e86f30ff3817)

> *Interactive Excel dashboard with slicers and charts to visualize coffee sales performance*

---

## Explore the Dashboard

This project demonstrates my skills in using Excel and Power Query to clean, analyze, and visualize sales data. It highlights how I build interactive dashboards that deliver clear business insights and support data-driven decisions.

For questions or further discussion, please don’t hesitate to connect with me via LinkedIn (link available in my GitHub profile).
