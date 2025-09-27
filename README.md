# Sales-Dashboard-PowerBI
Interactive Power BI dashboard for a chocolate manufacturing company. Includes data cleaning, star schema modeling, KPI tracking, team performance analysis, and product profitability insights based on Excel sales and shipment data.

Interactive Dashboard link : https://app.powerbi.com/view?r=eyJrIjoiZjhjMWFmM2UtYTI2My00MDVmLTk2YmYtY2NhODEyZmIxNzhlIiwidCI6IjJiYjZlNWJjLWMxMDktNDdmYi05NDMzLWMxYzZmNGZhMzNmZiIsImMiOjl9

# Chocolate Company Sales Dashboard 2025

## Objective
The goal of this project is to design and implement an **interactive Power BI dashboard** for a **chocolate manufacturing company**.  
The dashboard provides a **360° view of business operations**, including sales trends, team performance, and product profitability.  
Data is sourced from multiple **Excel files** and modeled using a **star schema** to support **data-driven decisions**.

## Use Case & Requirements
A chocolate manufacturing company approached us with multiple **Excel files containing shipment, sales, and product data** from 2023 and 2024.  
The client faced several challenges:

- **Disparate and messy data:** Data was scattered across multiple files with inconsistent formats, missing values, and duplicate entries.  
- **Lack of centralized reporting:** Management could not easily monitor sales, profits, or employee performance across regions and product categories.  
- **Limited insight into profitability:** The company struggled to identify high-margin products, underperforming items, and cost inefficiencies.  
- **Employee performance evaluation difficulties:** Sales teams and individual contributions were tracked manually, making performance comparison and recognition challenging.  

To address these needs, the client requested a **complete data analytics solution** that includes:

- **Data Cleaning and Transformation:** Standardize, deduplicate, and enrich the raw data to ensure accuracy and consistency across all sources.  
- **Data Modeling using Fact and Dimension Tables:**  
  <img width="1673" height="1112" alt="image" src="https://github.com/user-attachments/assets/6e561f28-8ad1-4154-8b39-37ec1e874139" />

- **Three-Page Interactive Power BI Dashboard:**  
  The client requested a **visual, interactive reporting solution** with three focus areas:  
  1. **Business Overview:** Provide high-level KPIs, trends, and regional insights to monitor overall company performance.  
  2. **Team Performance:** Evaluate individual employee contributions, team efficiency, and identify top performers to reward or replicate their strategies.  
  3. **Product & Profitability Analysis:** Identify high- and low-margin products, assess cost efficiency, and make informed production and marketing decisions.  


## Dashboard Overview

### Page 1 – Business Overview
**Purpose:** Provide a high-level snapshot of company performance.

<img width="2323" height="1316" alt="image" src="https://github.com/user-attachments/assets/3cfe923f-a7d7-41e6-8330-307f7a426e1a" />


**Contents:**
- KPI cards for Total Sales, Total Profit, Total Cost, and Boxes
- Dynamic parameter toggle for Sales, Profit, Cost, or Boxes
- Line chart showing monthly trend (2023–2024)
- Bar chart for count of Shipments by Order Status
- Pie chart showing regional distribution by selected parameter
- Slicers for Month, Year, and Category (Bars, Bites, Others)

### Page 2 – Team Performance
**Purpose:** Evaluate sales team and individual contributions.

<img width="2355" height="1316" alt="image" src="https://github.com/user-attachments/assets/65d12727-fbb3-4de8-b234-b9a2694e1b6c" />


**Contents:**
- KPI cards:
  - Best performing employee with total sales
  - Average Profit per Box
  - Average Sales per Employee
- Parameter toggle applied to:
  - Horizontal bar chart for categories
  - Leaderboard table: Employee, Team, Sales, Margin %, Target
  - Tree map of Products based on selected parameter

### Page 3 – Product & Profitability Analysis
**Purpose:** Assess profitability, cost efficiency, and product performance.

<img width="2333" height="1301" alt="image" src="https://github.com/user-attachments/assets/f61d517c-d9e9-43df-af47-df93080bddb1" />


**Contents:**
- Product Profitability Matrix: Cost per Box, Total Boxes, Total Cost, Total Profit, Margin %
- Conditional formatting for Margin Target (highlight if above 25%)
- Scatter plot: Total Profit vs Cost per Box

## Business Insights and Decisions

### Yearly Trends
- **2023:** Peak in January, drop from February to March, recovery from March–October, high in December.
- **2024:** Peak in February, drop in March, moderate growth until July, slight drop in August, recovery in September.  
  - July 2024: Boxes sold matched 2023, profit increased 54% → improved efficiency or pricing.

### Team and Employee Performance
- Top Salesperson: **Barr Faughny**  
- October 2024:
  - Highest Sales: **Husein Augar**
  - Highest Margin & Profit: **Camilla Castle**  
**Decision:** Recognize top-performing employees and replicate their strategies.

### Product Profitability
- **Dark Bars:** 37% margin loss (high cost per box = 10.51$)  
- **Caramel Stuffed Bars:** 3% margin → consider discontinuation  
- **Peanut Butter Cubes:** Highest profit margin (87%) and lowest cost  
**Decision:** Focus on high-margin products and review underperforming items.

## Technical Summary
**Tools Used:** Power BI, Excel

**Data Model:**
- **Fact Table:** `Fact_Shipments`  
  Contains transactional data: Sales, Cost, Profit, Boxes, Order Status, Shipment ID, Date, Employee ID, Product ID, Region ID
- **Dimension Tables:**
  - `Dim_Employee`
  - `Dim_Geo`
  - `Dim_Product`
  - `Calendar`

**Techniques Applied:**
- Star schema design
- Dynamic parameter switching
- Conditional formatting and margin targets
- Interactive slicers and filters
