<div align="center">

<!-- HERO BANNER -->
<img src="https://capsule-render.vercel.app/api?type=waving&color=006D6D&height=200&section=header&text=Restaurant%20Sales%20Insights&fontSize=42&fontColor=ffffff&fontAlignY=38&desc=Data-Driven%20Analysis%20of%20Restaurant%20Business%20Performance&descAlignY=58&descSize=16" width="100%"/>

# 🍽️ Restaurant Sales Insights Analysis

**Uncovering revenue patterns, menu performance, and business opportunities across 774K+ transactions**

<br/>

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![Excel](https://img.shields.io/badge/Microsoft%20Excel-217346?style=for-the-badge&logo=microsoftexcel&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![Data Analytics](https://img.shields.io/badge/Data%20Analytics-006D6D?style=for-the-badge&logo=databricks&logoColor=white)
![Dashboard](https://img.shields.io/badge/Dashboard-E8644A?style=for-the-badge&logo=googleanalytics&logoColor=white)

<br/>

![Status](https://img.shields.io/badge/Status-Completed-27AE60?style=flat-square)
![Rows](https://img.shields.io/badge/Dataset-774K%2B%20Rows-006D6D?style=flat-square)
![Restaurants](https://img.shields.io/badge/Restaurants-4%20Sites-F2A900?style=flat-square)
![Years](https://img.shields.io/badge/Period-2024%20–%202025-2E75B6?style=flat-square)

</div>

---

## 📌 Quick Navigation

| Section | Link |
|---|---|
| 📖 Project Overview | [Overview](#-project-overview) |
| ❓ Business Problem | [Problem](#-business-problem) |
| 🎯 Objectives | [Objectives](#-objectives) |
| 📊 Dataset | [Dataset](#-dataset-information) |
| 💡 Key Insights | [Insights](#-key-insights) |
| 🛠️ Tools Used | [Tools](#-tools-used) |
| 🚀 How to Use | [Usage](#-how-to-use) |
| 📈 Results & Impact | [Results](#-results--impact) |
| 🔮 Future Improvements | [Future](#-future-improvements) |
| 👤 Author | [Author](#-author) |

---

## 📖 Project Overview

> This project delivers a **comprehensive data analytics solution** for a multi-site restaurant business using real transactional data provided by **Dolphin Insights**.

The analysis covers **774,077 transactions** across **4 restaurant sites** spanning **May 2024 to July 2025**, examining year-on-year sales performance, menu profitability, discount strategy effectiveness, and site-level operational health.

A **5-page interactive Power BI dashboard** was built on top of a clean **star schema data model**, supported by **8 custom DAX measures** and a **financial calendar** for period-accurate time intelligence.

```
Total Net Sales    →    $12.78M
Total Transactions →    123K
YoY Growth         →    -4.31%
Avg Discount Rate  →    6.21%
Restaurants        →    4 Sites (London · Manchester · Liverpool · Birmingham)
```

---

## ❓ Business Problem

Restaurant businesses frequently operate without clear visibility into their own performance data. Common challenges include:

- 📉 **No clear picture of YoY revenue trends** across sites and time periods
- 🍔 **Unknown menu performance** — which items drive revenue and which erode margin
- 💸 **Uncontrolled discounting** — heavy discounts applied without understanding the margin impact
- 🏪 **Site-level blind spots** — underperforming locations identified too late
- 📅 **No financial calendar alignment** — standard date analysis misses business period patterns

This project addresses all of the above with a structured, data-driven analytical framework.

---

## 🎯 Objectives

- ✅ Analyze restaurant sales trends across financial periods, quarters, and weeks
- ✅ Identify top-performing and underperforming menu items and groups
- ✅ Track YoY revenue growth at both group and site level
- ✅ Measure and evaluate discount strategy effectiveness by menu group
- ✅ Profile data quality issues and document cleaning decisions
- ✅ Deliver actionable business recommendations based on findings
- ✅ Build an interactive, recruiter-ready Power BI dashboard

---

## 📊 Dataset Information

| Attribute | Detail |
|---|---|
| **Source** | Dolphin Insights (Assessment Dataset) |
| **Domain** | Restaurant Business Analytics |
| **Format** | Excel (.xlsx) — 5 sheets |
| **Total Rows** | 774,077 (after cleaning) |
| **Period Covered** | May 2024 – July 2025 |
| **Restaurants** | London, Manchester, Liverpool, Birmingham |

### 📋 Data Schema

```
📄 2024 Sheet          →  order_id, item_id, qty, gross, discount, net, transid, date, restaurant_id
📄 2025 Sheet          →  order_id, item_id, qty, gross, discount, net, transid, date, restaurant_id
📄 menu Sheet          →  group, family, name, num
📄 site Sheet          →  id, restaurant_name
📄 calendar Sheet      →  date, day, period, quarter, week_number, year, month_year,
                           quarter_year, period_number, quarter_number, month, month_number
```

### 🧹 Data Quality Actions

| Issue | Rows Affected | Action Taken |
|---|---|---|
| Blank row (null across all columns) | 1 | Removed |
| Zero quantity rows | 15 | Removed |
| Zero net rows (100% discounted) | 296,383 | Retained — valid business events |
| Zero discount rows | 720,939 | Retained — full-price transactions |

---



## 💡 Key Insights

### 📉 Overall Performance
- Total net sales of **$12.78M** recorded across May 2024 to July 2025
- YoY revenue declined **-4.31%** — 2024: $6.53M vs 2025: $6.25M
- All 4 restaurants experienced negative YoY growth — indicating a **systemic group-wide issue**

### 🏪 Site Performance
| Restaurant | 2024 Sales | 2025 Sales | YoY Change |
|---|---|---|---|
| 🥇 London | $2,147,641 | $2,072,185 | -3.51% |
| 🥈 Manchester | $1,624,233 | $1,558,141 | -4.07% |
| 🥉 Liverpool | $1,490,354 | $1,431,917 | -3.92% |
| ⚠️ Birmingham | $1,267,687 | $1,186,312 | **-6.42%** |

### 📅 Time Trends
- **Period 6** is the strongest financial period at **$7.4M** — 58% of total sales
- **Q2 FY24 ($6.5M) vs Q2 FY25 ($6.0M)** confirms a gradual decline not a sudden drop
- **Week 21** was the only week where 2025 surpassed 2024 performance

### 🍽️ Menu Performance
- **Sides group (21.sides)** is the highest revenue group at **$2.8M** — outselling all mains
- **Creamy Mushroom Curry** is the single best-selling item at **$811K** (22,339 qty)
- **Omakase group** carries a **74.92% discount rate** — a major margin erosion risk
- **Other-extras** discounted at **45.74%** — also requires pricing review

### 💸 Discount Analysis
```
Omakase        →  74.92%  ⚠️  Critical
Other-Extras   →  45.74%  ⚠️  High
Non-Alc Drinks →  16.06%  🔶  Moderate
Hot Beverages  →  13.80%  🔶  Moderate
Desserts       →  13.01%  🔶  Moderate
Sides          →   7.10%  ✅  Controlled
Kokoro         →   5.90%  ✅  Controlled
```

---

## 🛠️ Tools Used

<div align="center">

| Tool | Purpose | Version |
|---|---|---|
| ![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=flat-square&logo=powerbi&logoColor=black) | Dashboard, DAX, Data Modelling | Desktop Latest |
| ![Excel](https://img.shields.io/badge/Excel-217346?style=flat-square&logo=microsoftexcel&logoColor=white) | Data source, initial exploration | Microsoft 365 |
| ![Power Query](https://img.shields.io/badge/Power%20Query-006D6D?style=flat-square&logo=microsoft&logoColor=white) | ETL, data cleaning, append | M Language |
| ![DAX](https://img.shields.io/badge/DAX-E8644A?style=flat-square&logo=powerbi&logoColor=white) | Measures, KPIs, time intelligence | Power BI DAX |

</div>

### ⚙️ Key DAX Measures Built

```dax
Total Net Sales   = SUM(Sales[net])
Total Discount    = ABS(SUM(Sales[discount]))
Discount %        = DIVIDE([Total Discount], [Total Gross Sales], 0)
Total Orders      = DISTINCTCOUNT(Sales[transid])
Net Sales 2024    = CALCULATE([Total Net Sales], YEAR(Sales[date]) = 2024)
Net Sales 2025    = CALCULATE([Total Net Sales], YEAR(Sales[date]) = 2025)
YoY Growth %      = DIVIDE([Net Sales 2025] - [Net Sales 2024], [Net Sales 2024], 0)
Net Sales Change  = [Net Sales 2025] - [Net Sales 2024]
```


---

## 🚀 How to Use

### Step 1 — Clone the Repository
```bash
git clone https://github.com/ThAnalyser/restaurant-sales-insights.git
cd restaurant-sales-insights
```

### Step 2 — Open the Power BI Dashboard
```
1. Install Power BI Desktop (free) from microsoft.com/powerbi
2. Open powerbi/RestaurantSalesInsights.pbix
3. If prompted, update the data source path to your local data/ folder
4. Click Refresh to reload the data
```

### Step 3 — Explore the Dashboard
```
Page 1  →  Executive Summary    —  KPIs, YoY comparison, monthly trends
Page 2  →  Time Trends          —  Weekly, period, and quarter analysis
Page 3  →  Site Performance     —  Restaurant-level ranking and YoY table
Page 4  →  Menu Analysis        —  Revenue by group, discount by group, top items
Page 5  →  Key Insights         —  Summary findings and recommendations
```

### Step 4 — Interact with the Dashboard
```
✅ Use the Year slicer (2024 / 2025) to filter all visuals
✅ Click any bar to cross-filter related charts
✅ Hover over data points for detailed tooltips
✅ Use the group slicer on Menu Analysis to drill into specific categories
```

---

## 📈 Results & Impact

This analysis delivered the following measurable business value:

| Business Question | Answer Found |
|---|---|
| Is the business growing? | No — YoY decline of -4.31% across all sites |
| Which site needs attention? | Birmingham — steepest decline at -6.42% |
| Which site is most resilient? | London — least decline at -3.51% |
| What drives the most revenue? | Sides group ($2.8M) and Curry ($2.1M) |
| Is discounting controlled? | No — Omakase at 74.92% is a critical margin risk |
| What is the strongest period? | Period 6 at $7.4M — 58% of total revenue |
| Are there data quality issues? | Yes — identified, documented, and resolved |

**Business Recommendations Delivered:**
1. 🚨 Investigate Birmingham's -6.42% decline immediately
2. 💸 Cap Omakase discount rate — 74.92% is unsustainable
3. 🏆 Replicate London's operational model across other sites
4. 🍛 Promote high-revenue items (Creamy Mushroom Curry at $811K)
5. 📅 Conduct full-year 2025 review once complete data is available

---

## 🔮 Future Improvements

- 🤖 **Predictive Analytics** — Forecast next quarter sales using Python (Prophet or ARIMA)
- 👥 **Customer Segmentation** — RFM analysis to identify high-value customer groups
- 📦 **Inventory Optimization** — Link sales velocity to stock levels
- ⏰ **Peak Hour Analysis** — Add time-of-day dimension if granular data becomes available
- 🗺️ **Geospatial Analysis** — Map revenue by restaurant location using Power BI Maps
- 🔄 **Automated Data Refresh** — Connect to live data via Power BI Service + scheduled refresh
- 📱 **Mobile Dashboard** — Optimize layout for Power BI mobile app

---

## 👤 Author

<div align="center">

### Raja Hanzala Muavia

**Data Analyst | Power BI Developer | SQL | Python**

*BS Computer Science — Sindh Madarsatul Islam University, Karachi (Jan 2026)*

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/hanzalaraja)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/ThAnalyser)
[![Email](https://img.shields.io/badge/Email-Contact-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:hanzala.analyst@gmail.com)

**Core Skills:**
`Power BI` `DAX` `Power Query` `SQL` `Python` `Excel` `Star Schema` `Data Cleaning` `ETL`

**Certifications:**
`Microsoft Power BI Data Analyst Associate` `Google Data Analytics` `Microsoft Excel Associate` `SQL for Data Science (UC Davis)`

</div>

---

## 🤝 Acknowledgements

- **Dolphin Insights** — for providing the restaurant dataset as part of the Graduate Data Analyst assessment
- **Microsoft Power BI** — for the analytics and visualization platform
- **Power BI Community** — for DAX and modelling resources

---

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=006D6D&height=120&section=footer&text=Thank%20You%20for%20Visiting&fontSize=24&fontColor=ffffff&fontAlignY=65" width="100%"/>

**⭐ If you found this project useful, please consider giving it a star!**

*Built with dedication by [Raja Hanzala Muavia](https://linkedin.com/in/hanzalaraja)*

</div>
