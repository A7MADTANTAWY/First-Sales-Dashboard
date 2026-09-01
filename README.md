# 🛒 Sales Dashboard — Supermarket Analysis

An end-to-end **Power BI** sales dashboard built on a real supermarket transaction dataset. This project demonstrates the full data-analysis workflow — from raw CSV import and data modeling to interactive visualizations and a polished, professional dashboard report that tells a clear business story.

![Dashboard Preview](docs/Sales%20Dashboard_page-0001.jpg)

---

## 📌 Table of Contents

- [Overview](#overview)
- [Filters & Slicers](#filters--slicers)
- [KPI Cards — Key Metrics](#kpi-cards--key-metrics)
- [Visual Walkthrough](#visual-walkthrough)
- [Key Insights — The Story](#key-insights--the-story)
- [Interview Script](#interview-script)
- [Dataset](#dataset)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
- [Skills Demonstrated](#skills-demonstrated)
- [Technologies](#technologies)
- [Roadmap](#roadmap)
- [License](#license)

---

## 📖 Overview

This repository contains a complete business-intelligence project that transforms raw transaction-level supermarket sales data into an actionable **sales dashboard**. It answers key business questions such as:

- How are **revenue** and **profit** trending over time?
- Which **product lines** and **branches/cities** drive the most sales?
- What does the **customer base** (type & gender) look like, and how do they pay?

> **Most importantly**, the dashboard is not just about numbers — its goal is to surface **Insights and Business Decisions**: which branch performs best? Which product is the top seller? Who are the most valuable customers? When does demand peak? And when do sales drop?

---

## 🎛️ Filters & Slicers

The panel on the left is made of **Slicers / Filters** that dynamically change every visual in the dashboard based on your selections.

### Branch
- Options: `Branch A`, `Branch B`, `Branch C`
- Selecting e.g. `Branch A` filters **all** KPIs and charts to show `Branch A` data only.

### Month
- Options: `January`, `February`, `March`
- See sales performance for a specific month — e.g. selecting `February` updates `Total Sales`, `Sales by Day`, `Sales by Hour`, and so on.

### Payment
- Methods: `Cash`, `Credit card`, `Ewallet`
- Understand how customers pay and analyze whether `Credit card` drives higher sales than `Cash`.

### Gender
- `Female` and `Male`
- Segment sales by customer gender — e.g. do female customers generate more sales than male?

---

## 💎 KPI Cards — Key Metrics

The top section provides a quick **Executive Summary** so a manager can gauge sales health within seconds.

| Metric | Value | Explanation |
| --- | --- | --- |
| **Total Sales** | **322.97K** | Total sales value ≈ **322,970** over the dataset period. |
| **Total Margin** | **4.76%** | Profit margin: for every 100 of Sales, the company earns ≈ **4.76** in Profit. |
| **Total Profit** | **15.38K** | Total profit ≈ **15,380** = `Sales − COGS` = `322.97K − 307.59K`. |
| **Total Sold Items** | **6K** | Total items sold ≈ **6,000** (this is *not* the number of invoices). |
| **Total COGS** | **307.59K** | Cost of Goods Sold ≈ **307,590** — the cost of products sold. |
| **Average Invoice Value** | **322.97** | Average invoice value = `Total Sales ÷ Number of Invoices` (`322.97K ÷ ~1K`). |
| **Average Ratings** | **6.97** | Average transaction rating ≈ **7 out of 10**. |

**Analytical note:** The profit margin (4.76%) is relatively low compared to the volume of sales — a business can have large sales but a thin margin.

---

## 🖼️ Visual Walkthrough

### 1. Total Sales by City 🗺️
- Map in the top center showing sales by city.
- **Bubble size = sales volume** (bigger bubble → higher sales).
- Answers: which city generates the most sales? Where are the biggest spenders? Which city needs more marketing?

### 2. Sales By Branch 🍩
- Donut chart comparing the three branches:

| Branch | Sales |
| --- | --- |
| Branch C | **110.57K** |
| Branch A | **106.2K** |
| Branch B | **106.2K** |
| **Total** | **≈ 322.97K** |

- **Takeaway:** `Branch C` is the highest performer; `A` and `B` are very close — no huge gap, but `C` leads.

### 3. Sales By Customer Type 👥
- Splits customers into two types:

| Type | Sales |
| --- | --- |
| Member | **164.22K** |
| Normal | **158.74K** |

- `Members` out-sell `Normal` customers slightly (≈ 50.8% vs 49.2%) — a small gap.
- **Analytical question:** Does membership actually encourage more purchasing? A candidate for deeper analysis.

### 4. Top 6 Product Lines Sales 📊
- Bar chart of sales by product line.

| Product Line | Approx. Sales |
| --- | --- |
| Food and beverages | **56K** |
| Sports and travel | 55K |
| Electronic accessories | 54K |
| Fashion accessories | 54K |
| Home and lifestyle | 54K |
| Health and beauty | **49K** |

- **Highest:** `Food and beverages` (56K) — **Lowest:** `Health and beauty` (49K).
- The range is narrow, so sales are fairly evenly distributed across product lines.

### 5. Rating by Product Line ⭐
- Shows **average customer rating per product line** (not sales).

| Product Line | Rating |
| --- | --- |
| Food and beverages | **7.1** (highest) |
| Fashion accessories | 7.0 |
| Health and beauty | 7.0 |
| Electronic accessories | 6.9 |
| Sports and travel | 6.9 |
| Home and lifestyle | **6.8** (lowest) |

- **Key insight:** `Food and beverages` has both the **highest sales and highest rating**.
- `Health and beauty` rates well (7.0) but sells less — *why does a well-rated line under-sell?*

### 6. Rating by Branch 🌟
- Compares the average rating per branch.

| Branch | Rating |
| --- | --- |
| Branch C | **7.1** |
| Branch A | 7.0 |
| Branch B | 6.8–6.9 |

- `Branch C` has the highest rating **and** the highest sales — a strong **positive performance indicator**.

### 7. Sales by Day 📅
- Area/Line chart showing sales by day of the week.

| Day | Approx. Sales |
| --- | --- |
| Saturday | **163K** (best) |
| Tuesday | 158K |
| Wednesday | 143K |
| Friday | 139K |
| Thursday | 138K |
| Sunday | 133K |
| Monday | **125K** (weakest) |

- **Note:** days are ordered by sales value (highest → lowest), not chronologically.
- **Action:** stock up and staff up before `Saturday`; plan promotions to lift `Monday`.

### 8. Top Sales Hours ⏰
- X-axis: `Hour`, Y-axis: `Count of Invoice ID` — measures **number of invoices per hour**, not sales value.
- Data spans **10 AM → 8 PM** with a clear peak at **7 PM** (highest transaction count) and dips (e.g. around **5 PM**).
- **Action:** increase staff and inventory at the 7 PM peak; run targeted promotions; improve service during busy hours.

### 9. Sales by Month 📆
| Month | Approx. Sales |
| --- | --- |
| January | **116K** (highest) |
| February | **97K** (lowest) |
| March | **109K** |

- **Story:** January strong 📈 → February clear decline 📉 → March recovery 📈 (still below January).

---

## 🧭 Key Insights — The Story

Putting all the visuals together, the dashboard tells this story:

- 💰 **Sales:** The company generated **322.97K** in total sales.
- 💵 **Profit:** **15.38K** profit at a **4.76%** margin (relatively low).
- 🏢 **Branch Performance:** `Branch C` is the best on sales (**110.57K**) and also has the highest rating.
- 👥 **Customer Performance:** `Members` slightly out-sell `Normal` customers (**164.22K** vs **158.74K**).
- 🛍️ **Product Performance:** Top product line `Food and beverages` (**56K**), lowest `Health and beauty` (**49K**), with limited variation.
- ⭐ **Customer Satisfaction:** Best rating `Food and beverages` (**7.1**), lowest `Home and lifestyle` (**6.8**).
- 📅 **Time Analysis:** Best day `Saturday`, weakest `Monday`, peak transaction hour ≈ **7 PM**.
- 📆 **Monthly Trend:** `January` best → strong drop in `February` → `March` recovery.

---

## 🎤 Interview Script

A professional, concise summary you can say in an interview:

> *"This dashboard provides an overview of the company's sales performance across branches, customer types, product lines, and time periods. The business generated around 322.97K in total sales with 15.38K in profit and a 4.76% profit margin. Branch C was the highest-performing branch in terms of sales and also had the highest customer rating. Food and beverages was the top-performing product line by sales and rating. From the time analysis, Saturday generated the highest sales, while Monday was the weakest day, and the highest transaction activity occurred around 7 PM. Monthly analysis showed that January had the highest sales, followed by a significant decline in February and a recovery in March."*

**The key takeaway:** a dashboard isn't about stating "Sales = 322K" and stopping — it's about extracting **Insights** and driving **Business Decisions**.

---

## 🗂️ Dataset

A widely-used public **Supermarket Sales** sample: **3 months, 1,000 transactions (Jan–Mar 2019)** covering three branches in Myanmar.

| Column | Description |
| --- | --- |
| `Invoice ID` | Unique transaction identifier |
| `Branch` / `City` | Location of the sale |
| `Customer type` | `Member` or `Normal` |
| `Gender` | Customer gender |
| `Product line` | Product category |
| `Unit price` / `Quantity` | Price per unit and quantity sold |
| `Tax 5%` / `Total` | Tax and total amount |
| `Date` / `Time` | Transaction timestamp |
| `Payment` | Payment method (`Cash`, `Credit card`, `Ewallet`) |
| `cogs` / `gross income` | Cost of goods and gross profit |
| `gross margin percentage` | Margin percentage |
| `Rating` | Customer satisfaction rating |

**Source:** [Supermarket Sales — Kaggle](https://www.kaggle.com/datasets/aungpyaeap/supermarket-sales)

---

## 🗃️ Project Structure

```
First-Sales-Dashboard/
├── data/                             # Raw source data
│   └── supermarket_sales.csv
├── reports/                          # Interactive Power BI report (editable)
│   └── Sales Dashboard.pbix
├── docs/                             # Documentation & dashboard preview
│   └── Sales Dashboard_page-0001.jpg
├── README.md
└── .gitignore
```

---

## 🚀 Getting Started

### Prerequisites

- **Microsoft Power BI Desktop** (free) — to open & edit the `.pbix` file.

### Run it

1. Clone the repository:
   ```bash
   git clone https://github.com/<your-username>/First-Sales-Dashboard.git
   ```
2. Open **`reports/Sales Dashboard.pbix`** with Power BI Desktop.
3. The report and data model load automatically — no extra configuration needed.
4. Interact with the visuals, or print/export to PDF.

> Prefer a quick look? Open the **`docs/Sales Dashboard_page-0001.jpg`** preview.

---

## 🧠 Skills Demonstrated

- Data import, cleaning & shaping (Power Query)
- Data modeling & relationship design
- DAX measures for aggregations & KPIs
- Interactive report design & **storytelling with data**
- Professional formatting & layout
- Extracting actionable **insights & business decisions** from raw data

---

## 🛠️ Technologies

| Tool | Purpose |
| --- | --- |
| **Power BI Desktop** | Data modeling, DAX, and visualizations |
| **Power Query (M)** | Data transformation & cleaning |
| **DAX** | Custom measures & calculated columns |
| **CSV** | Raw data source |

---

## 🗺️ Roadmap

- [ ] Publish to the **Power BI Service** for live sharing
- [ ] Add an **Executive Summary** page
- [ ] Include a **Drill-through** page for product-line details
- [ ] Automate dataset refresh via a gateway

---

## 📄 License

This project is for **educational/portfolio purposes** and uses a publicly available sample dataset.

---

Made with ❤️ using **Microsoft Power BI**
