# Sales Dashboard - Supermarket Analysis

![Dashboard Preview](docs/Sales%20Dashboard_page-0001.jpg)

Power BI sales dashboard built from a single supermarket transactions dataset for portfolio use.

## Overview

The report tracks sales performance across branches, customer types, product lines, payment methods, gender, month, day, and hour.

## Dataset

`data/supermarket_sales.csv`

* 1,000 rows
* 17 columns
* January to March 2019
* Branches A, B, and C in Yangon, Mandalay, and Naypyitaw

## Dashboard

The dashboard includes:

* KPI cards for total sales, margin, profit, sold items, COGS, average invoice value, and average rating
* Sales by city map
* Sales by branch
* Sales by customer type
* Product line sales
* Rating by product line
* Rating by branch
* Sales by day
* Transaction volume by hour
* Sales by month

## Key KPIs

| KPI | Value |
|---|---:|
| Total Sales | 322,966.75 |
| Total Profit | 15,379.37 |
| Total COGS | 307,587.38 |
| Total Sold Items | 5,510 |
| Average Invoice Value | 322.97 |
| Average Rating | 6.97 |
| Profit Margin | 4.76% |

## Key Insights

* Branch C led sales and rating.
* Food and beverages was the top-performing product line.
* Members slightly outperformed Normal customers.
* Saturday was the strongest sales day; Monday was the weakest.
* Transaction volume peaked at 7 PM.
* January had the highest monthly sales.

## Tools & Technologies

* Power BI Desktop
* CSV

## Project Structure

```text
First-Sales-Dashboard/
├── README.md
├── .gitignore
├── data/
│   └── supermarket_sales.csv
├── dashboard/
│   └── supermarket_sales_dashboard.pbix
└── docs/
    └── Sales Dashboard_page-0001.jpg
```
