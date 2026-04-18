# 📊 Amazon Sales Analytics | Power BI Business Intelligence Dashboard

> **End-to-End BI Case Study | Star Schema | DAX | Executive Dashboards**


***

## 🧭 Overview

This project presents a **multi-layered Business Intelligence system** built on Amazon transactional sales data (2015–2020). It transforms raw order-level records into an executive-grade decision support tool — answering critical business questions around revenue, profitability, customer behavior, and operational performance.

> **Business Value:** Identifies where profit is being lost, which customers drive the most value, and whether the business is on track to hit its targets.

***

## 🎯 Problem Statement

E-commerce businesses generate massive transactional data but often lack structured insight to answer:

- Which products **drive revenue** vs. just volume?
- Who are the **most valuable customers**?
- Where is **profit being lost** — discounts, returns, or logistics?
- Is the business **meeting its revenue and profit targets**?

***

## 📁 Dataset

| Attribute | Details |
|---|---|
| **Source** | Amazon Sales Dataset |
| **Timeframe** | 2015 – 2020 |
| **Granularity** | Order-level transactions |
| **Volume** | 113K+ orders, 713K+ products sold |
| **Key Fields** | Customer demographics, Product hierarchy, Sales metrics, Operational data |

**Key Attributes include:**
- Customer: Age, Gender, Location
- Product: Category → Subcategory → Product Name
- Sales: Price, Quantity, Revenue, Profit, Discount
- Operations: Delivery Type, Order Status, Shipping Fee

***

## 🏗️ Data Model

A **Star Schema** architecture powers the entire analytics layer:

```
                    ┌──────────────┐
                    │  Dim_Customer │
                    └──────┬───────┘
                           │
┌──────────────┐    ┌──────▼────────┐    ┌──────────────┐
│  Dim_Product  │────│ Fact_Ecommerce│────│  Dim_Calendar │
└──────────────┘    └──────┬────────┘    └──────────────┘
                           │
                    ┌──────▼───────┐
                    │   Dim_Order  │
                    └──────────────┘
```

**Why Star Schema?**
- ⚡ Enables fast DAX aggregations
- 🔁 Simplifies time intelligence calculations
- 📈 Scales cleanly with more data or dimensions

***

## 📊 Dashboard Architecture (6 Analytical Layers)

### 1️⃣ Executive Overview — *What is happening?*
High-level KPIs for leadership. Tracks revenue trends, profit growth, and regional performance at a glance.

| KPI | Value |
|---|---|
| Total Revenue | $160M |
| Total Profit | $88M |
| Total Orders | 113K |
| Products Sold | 713K |
| Avg Rating | 2.73 / 5 |

**Key Insight:** Revenue grew sharply in 2020, but profit growth did not keep pace — signaling cost pressure and margin erosion.

***

### 2️⃣ Order Behavior Analysis — *Why are customers buying?*
Examines purchase patterns by demographics, delivery preferences, and order outcomes.

- Adults dominate purchases (~83% of orders)
- Gender split is balanced — no strong segment skew
- **~27% return rate** — a critical profitability risk

> 💡 High returns suggest product-expectation mismatch, description gaps, or logistics failures.

***

### 3️⃣ Product Performance — *What sells and what doesn't?*
Revenue and profit breakdown by category, subcategory, and SKU.

- Revenue is concentrated in a **few top-performing categories**
- Several products generate high volume but **low or negative margins**
- Signals the need for product portfolio rebalancing

***

### 4️⃣ Customer Insights — *Who are the valuable customers?*
Geographic revenue distribution and customer-level performance metrics.

- Strong geographic concentration in select regions
- Revenue per customer is stable over time → **low churn signal**
- 31K+ rating entries available for product feedback analysis

***

### 5️⃣ Profit Analysis & Forecasting — *Where is money made or lost?*
Profit dynamics, discount impact analysis, and time-series forecasting.

- Profit growth was flat until a **sharp uptick in 2020**
- Discounts are the **primary margin leak**
- Forecast shows continued upward trend if discount structure is corrected

***

### 6️⃣ Target vs. Performance — *Are we meeting goals?*
Variance analysis between planned and actual KPIs.

- Revenue: ~50% of target achieved
- Profit gap remains significant
- Incremental profit trend is slowly improving

***

## 💡 Key Business Insights

| # | Insight |
|---|---|
| 📈 | Revenue growth is strong, but **profit efficiency is weak** |
| 🔄 | A **~27% return rate** is materially harming profitability |
| 🛍️ | Revenue is **over-dependent** on a narrow product range |
| 🌍 | Geographic concentration creates **regional risk exposure** |
| 💸 | **Over-discounting** is the top margin erosion driver |
| 🎯 | Business is growing but **underperforming vs. targets** |

***

## 🚀 Strategic Recommendations

1. **Reduce Returns** — Improve product descriptions, images, and size guides; root-cause analysis on return reasons
2. **Fix Pricing Strategy** — Cut unnecessary discounting; explore dynamic pricing
3. **Prioritize High-Margin SKUs** — Shift focus from volume-driven to profit-driven product mix
4. **Segment Customers** — Build RFM-based segments for personalized campaigns
5. **Geographic Diversification** — Invest in underperforming regions to reduce concentration risk

***

## 🛠️ Technical Stack

| Tool | Usage |
|---|---|
| **Power BI Desktop** | Dashboard development |
| **DAX** | KPI measures, time intelligence, YoY ratios |
| **Star Schema** | Data modeling |
| **Power Query (M)** | Data transformation and cleaning |

**Advanced DAX Features Used:**
- Time intelligence (YoY growth, rolling averages)
- Dynamic KPI cards with conditional formatting
- Ratio measures (profit margin %, return rate %)
- Forecast line using Power BI analytics pane

***

## 📂 Repository Structure

```
📦 amazon-sales-analytics/
├── 📁 data/
│   └── amazon_sales_data.csv
├── 📁 dashboard/
│   └── Amazon_Sales_Analytics.pbix
├── 📁 screenshots/
│   ├── 01_executive_overview.png
│   ├── 02_order_behavior.png
│   ├── 03_product_performance.png
│   ├── 04_customer_insights.png
│   ├── 05_profit_forecast.png
│   └── 06_target_vs_actual.png
└── README.md
```

***

## ▶️ How to Run

1. Clone this repository
   ```bash
   git clone https://github.com/YOUR_USERNAME/amazon-sales-analytics.git
   ```
2. Open `dashboard/Amazon_Sales_Analytics.pbix` in **Power BI Desktop**
3. Use interactive filters:
   - 📅 Year (2015–2020)
   - 🗂️ Product Category
   - 👤 Customer Attributes (Age, Gender, Region)




