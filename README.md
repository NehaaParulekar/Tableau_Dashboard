<div align="center">

# 📊Tableau Dashboard Portfolio
This repository showcases interactive Tableau dashboards focused on extracting business insights from real-world datasets.
Built by [Neha Parulekar](https://github.com/NehaaParulekar)

</div>

---

## Dashboards

| # | Dashboard | Dataset | Charts | Live Demo |
|---|-----------|---------|--------|-----------|
| 1 | **HR Analytics** | HRDataset_v14 · 311 employees | 20 charts | [🚀 Open Dashboard](https://nehaaparulekar.github.io/Tableau_Dashboard/hr_dashboard.html) |
| 2 | **Netflix Content** | netflix.csv · 8,807 titles | 13 charts | [🚀 Open Dashboard](https://nehaaparulekar.github.io/Tableau_Dashboard/netflix_dashboard.html) |
| 3 | **Reliance industries analysis** | Reliance Industries · NSE: RELIANCE · 580 trading days (Jan 2024 – Mar 2026) | 15 charts · Candlestick · RSI · Bollinger Bands · Forecast | [🚀 Open Dashboard](https://nehaaparulekar.github.io/Tableau_Dashboard/reliance_dashboard.html) |
---

## 1 · HR Analytics Dashboard

This dashboard analyzes employee data to understand workforce trends and attrition patterns.
Key Focus Areas:
Employee attrition
Department-wise analysis
Job satisfaction levels
Salary and experience insights

> **Key finding:** Webster Butler has 61.9% team attrition. Production department at 39.7%. Both flagged automatically.

**20 interactive charts across 10 different chart types:**

- Waffle chart (gender) · Donut (status, race) · Lollipop (manager attrition)
- Scatter plot (salary vs engagement) · Dot plot (engagement deviation)
- Area line (hiring trend) · Diverging bar (days late, satisfaction)
- Stacked bar · Histogram · Horizontal & vertical bar charts

**8 KPI cards:** Total employees · Active · Attrition rate · Avg salary · Avg tenure · Engagement · Satisfaction · Diversity %

**Filters:** Department · Status · Performance · Gender · Source · Race · Hispanic/Latino · Marital status · Salary range · Name search

| Metric | Value |
|--------|-------|
| Total Employees | 311 |
| Attrition Rate | 33.4% |
| Avg Salary | $69,021 |
| Avg Tenure | 7.4 years |
| Diversity | 39.9% non-white |

---

### Business Recommendations:

HR:
Improve retention strategies for early-career employees
Focus on increasing job satisfaction through engagement initiatives
Review compensation structure for high-attrition roles 

---

## 2 · Netflix Content Analytics Dashboard

Netflix Dashboard Insights
Movies dominate Netflix content, contributing a higher percentage than TV shows
Significant increase in content additions observed after 2015
Drama and International content are among the most popular genres
United States and India are leading content producers
Peak content addition observed in recent years, indicating aggressive platform expansion

> **Key finding:** 2019 was Netflix's peak content year. Movies dominate at 69.6% of the catalogue.

**13 interactive charts:**

- Content trend by year · Movies vs TV shows · Rating distribution
- Top genres · Country breakdown · Duration analysis
- Monthly heatmap · Release year histogram

**Filters:** Content type · Rating · Country · Genre · Year range

| Metric | Value |
|--------|-------|
| Total Titles | 8,807 |
| Movies | 6,131 (69.6%) |
| TV Shows | 2,676 (30.4%) |
| Countries | 127 |
| Genres | 42 |
----

### Business Recommendations:


Netflix:
Invest more in high-performing genres like Drama and International content
Focus on regional content expansion (India, emerging markets)
Maintain consistent content release strategy 

---

## How to Use

1. Click a **Live Demo** link above
2. Click any chart bar, slice, or dot → all other charts update instantly
3. Use the **right sidebar** for precise filtering
4. Click **× on filter tags** to remove individual filters
5. Click **↺ Reset** to clear everything
6. Click **⬇ CSV** to export filtered data

---

## Tech Stack

```
Charts        Pure SVG (HR) · Chart.js (Netflix)
Data          Embedded — no server needed
Language      Vanilla JavaScript — no frameworks, no npm
Hosting       GitHub Pages
Dependencies  Zero (HR) · Chart.js CDN (Netflix)
```

---

## Repository Structure

```
Tableau_Dashboard/
├── hr_dashboard.html          ← HR Analytics (311 employees, 20 charts)
├── netflix_dashboard.html     ← Netflix Content Analytics (8,807 titles)
├── README.md                  ← This file
├── LICENSE                    ← MIT
└── .gitignore
```

---

## License

MIT — see [LICENSE](LICENSE)

---

<div align="center">

⭐ **Star this repo if you found it useful**

</div>
