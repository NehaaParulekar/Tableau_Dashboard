[README-2.md](https://github.com/user-attachments/files/26147372/README-2.md)

# Netflix Content Analytics Dashboard

**A fully interactive, self-contained analytics dashboard built from 8,807 Netflix titles.**
Cross-filter across 10 charts simultaneously — no server, no install, opens in any browser.

<br/>

[![Live Demo](https://img.shields.io/badge/🚀%20Live%20Demo-View%20Dashboard-E50914?style=for-the-badge)](https://NehaaParulekar.github.io/Tableau_Dashboard/netflix_dashboard.html)

<br/>

</div>

---

## 📌 Overview

This dashboard lets you explore the entire Netflix library interactively. Click any bar, donut slice, heatmap cell, or table row — every other chart updates instantly from real data. No approximations, no page reloads.

Built entirely with vanilla HTML, CSS, and JavaScript. The complete dataset (8,807 records) is embedded directly in the file as compact JSON — no API, no backend, no dependencies to install.

---

## ✨ What Makes It Different

| Feature | Detail |
|--------|--------|
| **True cross-filtering** | Every chart talks to every other chart in real time |
| **Real embedded data** | All 8,807 records in the file — not pre-aggregated summaries |
| **No flash on filter** | Uses `chart.update()` instead of destroy + recreate |
| **Export CSV** | Download the currently filtered dataset with one click |
| **Fully self-contained** | One `.html` file — share it, email it, open it offline |
| **Mobile responsive** | Layout reflows cleanly below 900px |

---

## 📊 Dashboard Preview

```
┌─────────────────────────────────────────────────────────────────────┐
│  N  Netflix Analytics                    [✕ Clear filters] [⬇ CSV] │
├──────────┬──────────────────────────────────────────────────────────┤
│          │  8,807  │  6,131  │  2,676  │  127  │  2019  │  99 min  │
│ FILTERS  ├─────────────────────────────┬────────────────────────────┤
│          │  Content Added Over Time    │  YoY Growth Rate           │
│ Type     │  (stacked bar · clickable)  │  (green/red bar)           │
│ Rating   ├──────────┬──────────────────┴────────────────────────────┤
│ Country  │  Donut   │  Rating Dist.  │  Release Year Timeline       │
│ Yr Range ├──────────┴────────────────┬───────────────────────────────┤
│          │  Top 15 Genres (stacked)  │  Top Countries (click rows)  │
│ [Reset]  ├────────────────────────────┼───────────────────────────────┤
│          │  Duration vs Year (bubble) │  Monthly Heatmap 2015–2021   │
│ Active   ├────────────────────────────┴───────────────────────────────┤
│ Filters  │  Genre Deep Dive Table  (click any row to cross-filter)   │
└──────────┴─────────────────────────────────────────────────────────┘
```

---

## 🗂 10 Interactive Charts

| # | Chart | Visualization | Click Action |
|---|-------|--------------|-------------|
| 1 | Content Added Over Time | Stacked bar | Filter by year added |
| 2 | Year-over-Year Growth | Bar (green/red) | Trend reference |
| 3 | Type Distribution | Donut | Filter Movie vs TV Show |
| 4 | Rating Distribution | Bar | Filter by rating |
| 5 | Release Year Timeline | Bar | Filter by release year |
| 6 | Top 15 Genres | Stacked horizontal bar | Filter by genre + see Movie/TV split |
| 7 | Movie Duration vs Release Year | Bubble/scatter | Visual distribution |
| 8 | Monthly Heatmap 2015–2021 | Custom HTML grid | Filter by exact month + year |
| 9 | Movie Runtime Breakdown | Donut | 5 runtime buckets |
| 10 | TV Show Seasons | Bar | Season distribution |

Plus a **Genre Deep Dive Table** — click any row to filter all charts instantly.

---

## 🔍 Key Insights

> These are real findings from the data — surfaced by the dashboard itself.

- 🇺🇸 **USA produces 41.9%** of all Netflix content — 3,689 titles
- 📈 **2019 was the peak year** — 1,999 titles added in a single year
- 📉 **2020–21 saw a decline** — COVID-19 disrupted global production pipelines
- 🚀 **2016 was the growth explosion** — +472.6% YoY as Netflix expanded globally
- 🌏 **India is #2** with 1,046+ titles — Bollywood's global reach is real
- 🎬 **Movies outnumber TV Shows 2.3:1** — 6,131 vs 2,676
- ⏱ **90–120 minutes is the sweet spot** — the most common movie runtime by far
- 📺 **67% of TV shows ran only 1 season** — 1,793 of 2,676

---

## 🛠 Tech Stack

```
Frontend        HTML5 · CSS3 · Vanilla JavaScript (ES2020)
Charts          Chart.js 4.4.1
Annotations     chartjs-plugin-annotation 3.1.0
Typography      Inter · Bebas Neue (Google Fonts)
Data            8,807 records embedded as compact JSON (312 KB)
Hosting         GitHub Pages (free)
```

**Zero npm. Zero build step. Zero server. Zero dependencies to install.**

---

## 🏗 Architecture

```
DATA LAYER
  312KB compact JSON embedded in HTML
  8,807 records → [type, ratingIdx, yearAdded, releaseYear,
                    month, genreIdxs[], countryIdxs[], extra]

STATE MANAGEMENT
  Single SEL object holds all active filters:
  Sidebar  → type, rating, country, yearFrom, yearTo
  Chart    → clickType, clickRating, clickCountry,
             clickGenre, clickReleaseYear, clickYearAdded, clickHeatCell

FILTER ENGINE  (runs on every interaction)
  computeVisible()  →  O(n) single pass over 8,807 records → visIds[]
  aggregate(visIds) →  counts all dimensions in one loop   → agg{}

RENDER
  10 chart builders read from agg{}
  chart.update('active') → smooth animated transitions, no repaint flash
```

---

## 🚀 Run Locally

```bash
# Clone the repo
git clone https://github.com/NehaaParulekar/Tableau_Dashboard.git

# Open the dashboard — no install needed
open Tableau_Dashboard/netflix_dashboard.html
```

Or just [download the HTML file](netflix_dashboard.html) and open it directly in any browser.

---

## 📁 Repository Structure

```
Tableau_Dashboard/
├── netflix_dashboard.html   ← The entire dashboard (open this)
├── netflix.csv              ← Source dataset from Kaggle
├── README.md                ← This file
├── LICENSE                  ← MIT License
└── .gitignore
```

---

## 📂 Dataset

**Source:** [Netflix Movies and TV Shows — Kaggle](https://www.kaggle.com/datasets/shivamb/netflix-shows) by Shivam Bansal

| Field | Description |
|-------|-------------|
| `type` | Movie or TV Show |
| `title` | Content title |
| `country` | Country of production |
| `date_added` | Date added to Netflix |
| `release_year` | Original release year |
| `rating` | Audience rating (TV-MA, R, PG-13…) |
| `duration` | Runtime in minutes or number of seasons |
| `listed_in` | Genre categories |

**8,807 titles · 127 countries · 42 genres · Data through 2021**

---

## 📄 License

Released under the [MIT License](LICENSE) — free to use, modify, and distribute.

---

<div align="center">

**Built by [Neha Parulekar](https://github.com/NehaaParulekar)**

⭐ Star this repo if you found it useful

</div>
