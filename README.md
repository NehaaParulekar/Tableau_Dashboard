
























<div align="center">

# 📊 Tableau Dashboard Portfolio

This repository showcases interactive Tableau dashboards focused on extracting business insights from real-world datasets.

Built by [Neha Parulekar](https://github.com/NehaaParulekar)
</div>


## 1 ·👩‍💼 HR Analytics Dashboard
This dashboard analyzes employee data to understand workforce trends and attrition patterns.

**Key Focus Areas:**

* Employee attrition
* Department-wise analysis
* Job satisfaction levels
* Salary and experience insights

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

## 2 · Netflix Content Analytics Dashboard

This dashboard explores Netflix’s content library to identify trends in movies and TV shows.

**Key Focus Areas:**

* Content distribution (Movies vs TV Shows)
* Genre popularity
* Year-wise content growth
* Country-wise production

### 🎬 Netflix Dashboard Insights

* Movies dominate Netflix content, contributing a higher percentage than TV shows
* Significant increase in content additions observed after 2015
* Drama and International content are among the most popular genres
* United States and India are leading content producers
* Peak content addition observed in recent years, indicating aggressive platform expansion
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

### 👩‍💼 HR Dashboard Insights

* Higher attrition observed among employees with lower experience levels
