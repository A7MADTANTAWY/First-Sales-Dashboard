# 🛒 Sales Dashboard — Supermarket Analysis

An end-to-end **Power BI** sales dashboard built on a real supermarket transaction dataset. This project demonstrates the full data-analysis workflow — from raw CSV import and data modeling to interactive visualizations and a polished, professional dashboard report.

![Dashboard Preview](Sales%20Dashboard_page-0001.jpg)

---

## 📌 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Dataset](#dataset)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
- [Dashboard Highlights](#dashboard-highlights)
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

The deliverables include the interactive **Power BI report** (`.pbix`), an exported **PDF** version, and a **visual preview** of the dashboard.

---

## ✨ Features

- **Interactive filters & slicers** — explore by city, date range, payment method, and customer type.
- **KPI cards** — revenue, gross income, and key metrics at a glance.
- **Time-series analysis** — monthly sales & revenue trends.
- **Category breakdown** — performance by product line.
- **Branch & city comparison** — performance across Yangon, Mandalay, and Naypyitaw.
- **Customer & payment insights** — segmentation by customer type, gender, and payment method.

---

## 🗂️ Dataset

The dataset is a widely-used public **Supermarket Sales** sample (3 months, 1,000 transactions, Jan–Mar 2019) covering three branches in Myanmar.

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
├── Sales Dashboard.pbix              # Interactive Power BI report (editable)
├── Sales Dashboard.pdf               # Exported static report
├── Sales Dashboard_page-0001.jpg     # Dashboard preview image
└── supermarket_sales.csv             # Raw source data
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
2. Open **`Sales Dashboard.pbix`** with Power BI Desktop.
3. The report and data model load automatically — no extra configuration needed.
4. Interact with the visuals, or print/export to PDF.

> Prefer a quick look? Open the **`Sales Dashboard.pdf`** or the **`.jpg` preview**.

---

## 📊 Dashboard Highlights

- Comprehensive KPIs for **total revenue**, **gross income**, and transaction **rating**.
- **Sales by branch & city** to identify top-performing locations.
- **Revenue by product line** to reveal the best-sellers (e.g., Food and beverages, Electronic accessories).
- **Payment method distribution** for operational planning.
- **Gender & customer-type segmentation** to refine marketing strategies.

---

## 🧠 Skills Demonstrated

- Data import, cleaning & shaping (Power Query)
- Data modeling & relationship design
- DAX measures for aggregations & KPIs
- Interactive report design & storytelling with data
- Professional formatting & layout

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
