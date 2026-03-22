<div align="center">
# HR Analytics Dashboard

**Fully interactive HR analytics dashboard — 20 cross-filterable charts, 8 KPI cards, zero external dependencies.**

Click any chart → every other chart, KPI, and the employee table updates instantly from real data.

<br/>

[![Live Demo](https://img.shields.io/badge/🚀%20Open%20Dashboard-Live%20Demo-2D5F8A?style=for-the-badge)](https://NehaaParulekar.github.io/Tableau_Dashboard/hr_dashboard.html)

</div>

---

## Dashboards in this repo

| Dashboard | Description | Link |
|-----------|-------------|------|
| **HR Analytics** | 311 employees · 20 charts · cross-filtering | [Open →](https://nehaaparulekar.github.io/Tableau_Dashboard/hr_dashboard.html) |
| **Netflix Analytics** | 8,807 titles · genre, rating, country analysis | [Open →](https://nehaaparulekar.github.io/Tableau_Dashboard/netflix_dashboard.html) |
| **Universal Dashboard** | Drop any CSV/JSON — auto-generates charts | [Open →](https://nehaaparulekar.github.io/Tableau_Dashboard/dashboard.html) |

---

## Key HR Metrics

| Metric | Value |
|--------|-------|
| Total Employees | 311 |
| Active | 207 (66.6%) |
| Attrition Rate | 33.4% |
| Average Salary | $69,021 |
| Average Tenure | 7.4 years |
| Average Engagement | 4.12 / 5.0 |
| Diversity | 39.9% non-white |

---

## 20 Interactive Charts — 10 Chart Types

| Section | Chart | Type |
|---------|-------|------|
| Workforce | By Department | Horizontal bar |
| Workforce | Employment Status | Donut |
| Workforce | Gender Split | Waffle chart |
| Workforce | Performance Score | Horizontal bar |
| Retention | Attrition by Department | Vertical bar + avg line |
| Retention | Manager Attrition | Lollipop chart |
| Retention | Termination Reasons | Horizontal bar |
| Compensation | Salary vs Engagement | Scatter plot |
| Compensation | Salary by Department | Vertical bar |
| Compensation | Engagement Score | Dot plot |
| Compensation | Tenure by Department | Horizontal bar |
| Behaviour | Days Late by Performance | Diverging bar |
| Behaviour | Absences by Department | Vertical bar |
| Behaviour | Special Projects | Horizontal bar |
| Pipeline | Recruitment Source | Horizontal bar |
| Pipeline | Race / Ethnicity | Donut |
| Pipeline | Hiring Trend | Area line chart |
| Pipeline | Salary Distribution | Histogram |
| Pipeline | Employee Satisfaction | Stacked diverging bar |
| Pipeline | Top Positions | Horizontal bar |

---

## Critical Insights in the Data

- **Webster Butler: 61.9% team attrition** — flagged by crisis alert on load
- **Kissy Sullivan: 54.5% team attrition** — visible in lollipop chart
- **Production: 39.7% attrition** — shown in red (≥35% threshold)
- **PIP employees: 4.31 avg days late vs 0.00 for Exceeds** — diverging bar
- **IT/IS earns 62% more than Production** — $97K vs $60K
- **"Another position"** is the #1 voluntary exit reason

---

## How to Use

1. **Open** the dashboard — loads in under 1 second (no CDN)
2. **Click any chart bar, slice, or dot** → all 20 charts filter instantly
3. **Use the right sidebar** → dropdowns + salary slider
4. **Active filter tags** at sidebar bottom → click `×` to remove individually
5. **Reset** button → clears all filters
6. **CSV export** → downloads the currently filtered employee list
7. **Print** → opens browser print dialog for PDF

---

## Why it's fast

**Zero external requests.** No Chart.js CDN, no Google Fonts, no analytics scripts. Everything — charts, data, styles — is baked into one HTML file.

**Compressed data.** The 311 employee records are encoded as integer arrays (categorical fields become index references to lookup tables), shrinking the data from 131KB to 23KB.

**Pure SVG charts.** A hand-built SVG chart engine replaces Chart.js entirely. No canvas, no WebGL, no library overhead.

---

## Tech Stack

```
Charts        10 SVG chart types (bar, donut, scatter, lollipop, waffle, etc.)
Data          311 records compressed from 131KB → 23KB integer encoding
Fonts         System fonts — zero load time
Language      Vanilla JavaScript (ES5, no transpiler)
Total size    ~83KB — one self-contained HTML file
Dependencies  ZERO
```

---

## Dataset

**Source:** HRDataset_v14 (New England College of Business, Dr. Carla Patalano)

311 employees · 36 original fields · data through 2020

---

## License

MIT © 2024 [Neha Parulekar](https://github.com/NehaaParulekar)
