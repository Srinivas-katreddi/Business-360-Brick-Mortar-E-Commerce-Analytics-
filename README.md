# 📊 Business 360 – Brick & Mortar & E-Commerce Analytics

![Power BI](https://img.shields.io/badge/Power%20BI-Analytics-yellow)
![MySQL](https://img.shields.io/badge/MySQL-Database-blue)
![Power Query](https://img.shields.io/badge/Power%20Query-ETL-green)
![DAX](https://img.shields.io/badge/DAX-Data%20Analysis-orange)
![Data Analytics](https://img.shields.io/badge/Data%20Analytics-Business%20Intelligence-purple)

## 📌 Project Overview

**Business 360** is an end-to-end **Business Intelligence and Data Analytics project** developed for **AtliQ Hardware**.

The objective of this project is to provide a **360-degree view of business performance** by integrating and analyzing data across different business functions such as:

- 💰 Finance
- 📈 Sales
- 📣 Marketing
- 🚚 Supply Chain
- 👔 Executive Management

The project transforms raw business data into interactive and meaningful dashboards using **MySQL, Power Query, Power BI, and DAX**, helping stakeholders understand business performance and identify important trends.

---

## 🎯 Business Problem

AtliQ Hardware operates across different markets and business channels, generating large amounts of data from customers, products, sales, forecasts, costs, and other business operations.

Analyzing these datasets independently makes it difficult to get a complete picture of the organization's performance.

This project addresses the problem by creating a centralized analytical solution that allows users to:

- Monitor key business KPIs
- Analyze sales and profitability
- Compare current performance with previous years
- Identify high and low-performing products
- Analyze customer performance
- Evaluate regional and market performance
- Track forecast accuracy
- Understand cost and expense structures
- Support data-driven business decisions

---

# 🏗️ Data Model

The Power BI solution uses a structured dimensional data model consisting of **fact and dimension tables**.

### Dimension Tables

- `dim_date`
- `dim_product`
- `dim_customer`
- `dim_market`
- `fiscal_year`

### Fact Tables

- `fact_forecast_monthly`
- `fact_actuals_estimates`
- `post_invoice_deductions`
- `manufacturing_cost`
- `freight_cost`
- `operational_expense`

The model connects business dimensions with transactional and financial facts to enable flexible analysis across different business perspectives.

---

# 🔄 Data Pipeline

The overall data flow used in the project is:

```text
MySQL Database
       ↓
Data Extraction
       ↓
Power Query
       ↓
Data Cleaning & Transformation
       ↓
Data Modeling
       ↓
DAX Measures & KPIs
       ↓
Power BI Dashboards
       ↓
Business Insights
````

---

# 🛠️ Tools & Technologies

| Technology        | Purpose                                                  |
| ----------------- | -------------------------------------------------------- |
| **MySQL**         | Data storage and data extraction                         |
| **Power Query**   | Data cleaning and transformation                         |
| **Power BI**      | Dashboard development and visualization                  |
| **DAX**           | Calculated measures and business KPIs                    |
| **Data Modeling** | Creating relationships between fact and dimension tables |
| **Excel / CSV**   | Supporting data sources where applicable                 |

---

# 📊 Dashboard Views

The project contains multiple analytical views designed for different business functions.

## 1️⃣ Executive View

Provides a high-level overview of the organization's performance.

### Key KPIs

* Net Sales
* Gross Margin %
* Net Profit %
* Year-over-Year Growth
* Regional Performance
* Product Performance
* Customer Performance

This view helps management quickly understand the overall health of the business.

---

## 2️⃣ Finance View 💰

The Finance dashboard provides a detailed **Profit & Loss Statement**.

### Metrics Analyzed

* Gross Sales
* Pre-Invoice Deductions
* Net Invoice Sales
* Post-Invoice Deductions
* Net Sales
* Manufacturing Cost
* Freight Cost
* Other Costs
* Total COGS
* Gross Margin
* Gross Margin %
* Operating Expense
* Net Profit

It also provides **Year-over-Year comparisons** to understand changes in financial performance.

---

## 3️⃣ Sales View 📈

The Sales dashboard focuses on customer and product performance.

### Analysis Includes

* Customer-wise Net Sales
* Gross Margin
* Gross Margin %
* Product Performance
* Segment Performance
* Region / Market / Customer performance
* Net Sales trends
* Profitability analysis

The dashboard also provides a **Performance Matrix** to compare products based on sales and gross margin.

---

## 4️⃣ Marketing View 📣

The Marketing dashboard helps analyze product and customer profitability.

### Key Analysis

* Product performance
* Customer performance
* Net Sales
* Gross Margin
* Gross Margin %
* Profitability / Growth Matrix
* Regional performance
* Market performance

This helps identify areas contributing positively or negatively to business profitability.

---

## 5️⃣ Supply Chain View 🚚

The Supply Chain dashboard focuses on forecasting and inventory-related performance.

### Key Metrics

* Forecast Accuracy %
* Forecast Accuracy % LY
* Net Error
* Net Error %
* Risk Classification
* Customer-level forecast performance
* Product / Segment-level forecast performance

Customers and products can be analyzed based on their forecast accuracy and associated risk.

---

## 6️⃣ Performance Analysis

Interactive performance matrices were created to compare different business entities.

### Examples

* Product vs Gross Margin
* Product vs Net Sales
* Customer vs Gross Margin
* Customer vs Net Sales
* Region vs Gross Margin
* Market vs Gross Margin

These visualizations make it easier to identify business segments requiring further investigation.

---

# 📈 Key KPIs

Some of the important KPIs implemented in the dashboard include:

### Sales KPIs

* Net Sales
* Gross Sales
* Net Invoice Sales
* Sales Growth %

### Profitability KPIs

* Gross Margin
* Gross Margin %
* Net Profit
* Net Profit %
* Operating Expense
* Total COGS

### Supply Chain KPIs

* Forecast Accuracy %
* Forecast Accuracy % LY
* Net Error
* Net Error %

### Time Intelligence

* Current Year
* Previous Year
* Year-over-Year Change
* Year-over-Year Change %
* YTD
* YTG
* Quarterly Analysis
* Monthly Analysis

---

# 🧮 DAX & Data Analysis

DAX was used to create business measures and analytical calculations.

The project uses DAX for:

* KPI calculations
* Year-over-Year analysis
* Time intelligence
* Profitability calculations
* Gross Margin calculations
* Net Profit calculations
* Growth analysis
* Forecast accuracy
* Dynamic dashboard metrics

Example measures include:

```DAX
Gross Margin % =
DIVIDE(
    [Gross Margin],
    [Net Sales]
)
```

```DAX
Net Profit % =
DIVIDE(
    [Net Profit],
    [Net Sales]
)
```

```DAX
Sales YTD =
TOTALYTD(
    [Net Sales],
    dim_date[date]
)
```

---

# 🔍 Interactive Features

The dashboard provides interactive capabilities including:

* Region / Market filtering
* Customer filtering
* Product / Segment filtering
* Year selection
* Quarter selection
* YTD / YTG analysis
* Drill-down analysis
* Product performance analysis
* Customer performance analysis
* Dynamic KPI cards
* Performance matrices

These features allow users to move from a high-level overview to detailed business-level analysis.

---

# 📷 Dashboard Screenshots

## Executive / Supply Chain View

![Executive Dashboard](images/executive-view.png)

---

## Sales / Product Performance

![Sales Dashboard](images/sales-view.png)

---

## Customer Performance

![Customer Dashboard](images/customer-view.png)

---

## Finance / Profit & Loss

![Finance Dashboard](images/finance-view.png)

---

## Business 360 Navigation

![Business 360 Home](images/business-360-home.png)

> **Note:** Update the image paths above according to the actual screenshot filenames in the repository.

---

# 📂 Project Structure

```text
Business-360-Brick-Mortar-E-Commerce-Analytics/
│
├── 📊 Power BI/
│   └── Business 360 Dashboard
│
├── 📁 Data/
│   ├── Dimension Data
│   └── Fact Data
│
├── 📁 SQL/
│   └── SQL Queries
│
├── 📁 Screenshots/
│   └── Dashboard Screenshots
│
└── README.md
```

> The folder structure may vary depending on the files included in the repository.

---

# 💡 Business Insights

The dashboard enables stakeholders to investigate questions such as:

### Sales

* Which customers generate the highest sales?
* Which products or segments contribute the most revenue?
* How are sales changing over time?
* Which regions and markets generate the highest sales?

### Finance

* What is the current Gross Margin?
* How much does each cost category contribute to total COGS?
* How are operating expenses affecting profitability?
* How has Net Profit changed compared with the previous year?

### Marketing

* Which products have strong sales but lower margins?
* Which customers generate higher profitability?
* Which regions have stronger margins?

### Supply Chain

* Which customers have lower forecast accuracy?
* Where is forecast error high?
* Which products or segments require attention?
* Which areas show potential inventory risk?

---

# 🚀 Learning Outcomes

Through this project, I strengthened my practical knowledge of:

* Data Cleaning
* ETL using Power Query
* SQL & MySQL
* Data Modeling
* Star Schema Concepts
* DAX
* Time Intelligence
* KPI Development
* Business Intelligence
* Interactive Dashboard Design
* Data Visualization
* Business-Oriented Data Analysis

Most importantly, this project helped me understand how to move from:

**Raw Data → Clean Data → Data Model → DAX → Visualization → Business Insights**

---

# 🔗 Project Repository

GitHub:

**[Business 360 – Brick & Mortar & E-Commerce Analytics](https://github.com/Srinivas-katreddi/Business-360-Brick-Mortar-E-Commerce-Analytics-)**

---

# 👨‍💻 Author

### KATREDDI SAI SRINIVAS

🎓 B.Tech – Computer Science & Engineering

💻 Interested in:

* Data Analytics
* Business Intelligence
* Power BI
* SQL
* Data Visualization
* Software Development

---

## ⭐ If you find this project useful

Feel free to **star ⭐ the repository** and explore the project.

Feedback and suggestions are always welcome!

---

### 🏷️ Tags

`Power BI` `MySQL` `Power Query` `DAX` `Data Analytics` `Business Intelligence` `Data Visualization` `SQL` `Data Modeling` `Dashboard` `Business Analytics`

````
