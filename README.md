# GTA Franchise – India Gaming Sales & Profitability Analysis

## Project Overview

The **GTA Franchise – India Gaming Sales & Profitability Analysis** project focuses on analysing simulated video game sales data to understand sales performance, revenue, estimated costs, and profitability across different games, platforms, states, cities, and regions in India.

The project uses **Microsoft Excel** for data cleaning and quality checks and **Power BI** for data modelling, DAX calculations, interactive visualisations, and dashboard development.

## Project Objectives

- Analyse total units sold across GTA game titles.
- Calculate estimated revenue, costs, and profit.
- Compare game-wise and platform-wise performance.
- Identify top-performing Indian states and cities.
- Analyse regional sales distribution.
- Understand sales trends over time.
- Present business insights through interactive dashboards.

## Tools & Technologies

| Tool | Purpose |
|---|---|
| Microsoft Excel | Data cleaning and data quality checks |
| Power BI | Dashboard development and visualisation |
| Power Query | Data transformation |
| DAX | Measures and business calculations |

## Dataset Description

The dataset contains simulated gaming sales information with fields such as:

- Order Date
- Game Title
- Platform
- Units Sold
- Unit Selling Price (INR)
- Estimated Unit Cost (INR)
- State
- City
- Region

**Note:** This is an illustrative project using simulated data. The sales, revenue, cost, profit, and India location figures do not represent actual Rockstar Games business performance or official sales figures.

## Data Cleaning – Microsoft Excel

The dataset was prepared using Microsoft Excel.

Key activities included:

- Identifying missing values.
- Checking unknown state and city entries.
- Reviewing data quality issues.
- Maintaining a separate Data Quality Log.
- Preparing a cleaned dataset for Power BI analysis.

### Data Quality Summary

| Data Quality Issue | Records |
|---|---:|
| Missing Units Sold | 9 |
| Missing Unit Selling Price | 7 |
| Unknown State | 63 |
| Unknown City | 49 |

Missing numeric values were retained as blank, and unknown location values were preserved for transparency. Unknown locations are excluded from state and city rankings and map analysis.

## Power BI – Dashboard Development

The report is planned across three analytical pages.

### Page 1 – Game Performance Analysis

Planned analysis:
- Total Units Sold
- Total Revenue
- Estimated Profit
- Profit Margin
- Game-wise performance
- Platform-wise sales comparison

### Page 2 – India State-wise Analysis

Dashboard visuals include:
- Total Units Sold
- Total Revenue
- Estimated Profit
- Profit Margin
- Region-wise revenue comparison
- Top 10 states by estimated revenue
- City-wise estimated revenue
- India sales distribution map

### Page 3 – Sales Trend & Growth Analysis

Planned analysis:
- Monthly sales trends
- Revenue growth analysis
- Game-wise sales trends
- Platform-wise performance over time

## DAX Measures

Some important measures created for the analysis:

**1. Total Units Sold**
```DAX
Total Units Sold =
SUM('Clean_Data'[Units_Sold])
```

**2. Total Revenue**
```DAX
Total Revenue =
SUMX(
    'Clean_Data',
    'Clean_Data'[Units_Sold] *
    'Clean_Data'[Unit_Selling_Price_INR]
)
```

**3. Estimated Total Cost**
```DAX
Estimated Total Cost =
SUMX(
    'Clean_Data',
    'Clean_Data'[Units_Sold] *
    'Clean_Data'[Estimated_Unit_Cost_INR]
)
```

**4. Estimated Profit**
```DAX
Estimated Profit =
[Total Revenue] - [Estimated Total Cost]
```

**5. Profit Margin**
```DAX
Profit Margin % =
DIVIDE(
    [Estimated Profit],
    [Total Revenue],
    0
)
```

## Key Business Questions

This project aims to answer questions such as:

1. Which GTA game has the highest estimated revenue?
2. Which platform contributes the most units sold?
3. Which Indian states have the highest estimated revenue?
4. Which cities contribute the most to sales?
5. Which region performs best?
6. How do sales and revenue change over time?
7. What is the estimated profit margin?

## Expected Outcomes

- Better understanding of gaming sales performance.
- Identification of top-performing games and platforms.
- Comparison of simulated sales across Indian locations.
- Clear visibility into estimated revenue and profitability.
- Interactive dashboards to support data-driven analysis.

## Project Status

The Excel data preparation and initial Power BI dashboard development have been completed. The three-page report is being developed, with further visual formatting and analysis in progress.

---

**Project Type:** Data Analytics | Portfolio Project  
**Domain:** Gaming & Entertainment  
**Tools:** Excel | Power BI | Power Query | DAX
