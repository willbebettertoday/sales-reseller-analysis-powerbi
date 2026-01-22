# 📊 Sales Performance & Reseller Analysis Dashboard

**An interactive Business Intelligence solution designed to analyze global retail sales, identify revenue drivers, and assess partner performance.**

> *Note: This repository contains the source `.pbix` file. To interact with the full report (filters, drill-throughs), please download the file and open it in Microsoft Power BI Desktop.*

---

## 🚀 Project Overview

This project transforms raw transactional data into actionable insights for strategic decision-making. The dashboard enables sales managers to monitor high-level KPIs while providing granular tools to identify underperforming products and "at-risk" resellers.

**Key Business Questions Answered:**
* How is the company performing Year-over-Year across different regions?
* Which specific products generate 80% of our revenue? (Pareto Principle)
* Which resellers are failing to meet their quotas despite high revenue?

---

## 📸 Dashboard Highlights

### 1. Executive Sales Overview
A comprehensive view of business health.
* **KPIs:** Total Revenue ($109M), Gross Margin, Sold Units, and YoY Growth.
* **Channel Analysis:** Clear split between Internet Sales vs. Reseller Revenue.
* **Geography:** Regional performance breakdown.

![Executive Overview](./executive_overview.png)

### 2. Product Pareto Analysis (80/20 Rule)
A dynamic analysis identifying the "vital few" products.
* **Logic:** The combination chart visualizes that a small percentage of products drives the majority of revenue.
* **Actionable Insight:** Allows the supply chain team to prioritize inventory for high-impact items (Green bars).

![Pareto Analysis](./pareto_analysis.png)

### 3. Reseller Risk Assessment
A strategic tool for partner management.
* **Clustering:** Resellers are plotted by **Margin %** vs. **Quota Attainment %**.
* **Status Logic:** Partners are automatically classified as **"Healthy"** (Green) or **"At Risk"** (Red/Yellow) based on performance thresholds.
* **Detail View:** Heatmap table highlights specific gaps in quota achievement.

![Reseller Risk Analysis](./reseller_risk.png)

---

## 🛠 Tech Stack & Methodology

* **Tool:** Microsoft Power BI Desktop
* **ETL (Extract, Transform, Load):**
    * Used **Power Query** to clean messy raw data.
    * Standardized currency formats and date fields.
* **Data Modeling:**
    * Built a robust **Star Schema**.
    * Fact Tables: `FactResellerSales`, `FactInternetSales`.
    * Dimension Tables: `DimProduct`, `DimReseller`, `DimDate`, `DimGeography`.
* **Advanced DAX Measures:**
    * `YoY Growth %` = `(Current Sales - Previous Year Sales) / Previous Year Sales`
    * `Pareto Cumulative %` = `DIVIDE(Running Total, Total Sales)`
    * Dynamic segmentation logic for Reseller Status.

---

## 📂 Repository Structure

* `Sales Analysis Dashboard.pbix` - The main Power BI file.
* `executive_overview.png` - Screenshot of the main dashboard page.
* `pareto_analysis.png` - Screenshot of the product analysis page.
* `reseller_risk.png` - Screenshot of the partner analysis page.

---
*Created by Danil Sysenko. Open for Data Analysis & BI opportunities.*
