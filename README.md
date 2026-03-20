# 🎬 Netflix Content Analytics Dashboard

An **interactive, self-contained** analytics dashboard for the Netflix Movies & TV Shows dataset. Every chart is cross-filterable — click any bar, slice, row, or heatmap cell and every other chart updates instantly. No server, no install. Just open the HTML file.

---

## 🚀 Live Demo

> **GitHub Pages:** `https://YOUR_USERNAME.github.io/netflix-dashboard/netflix_dashboard.html`
> *(Enable: Settings → Pages → Source: `main` branch → `/root`)*

---

## ✨ Features

### 10 Fully Interactive Charts
| Chart | Type | Click to Filter |
|-------|------|----------------|
| Content Added Over Time | Stacked bar | ✅ By year added |
| Year-over-Year Growth | Bar | % change trend |
| Type Distribution | Donut | ✅ Movie vs TV Show |
| Rating Distribution | Bar | ✅ By audience rating |
| Release Year Timeline | Bar | ✅ By release year |
| Top 15 Genres (stacked) | Horizontal bar | ✅ Genre + Movie/TV split |
| Movie Duration vs Year | Bubble/scatter | Distribution shift |
| Monthly Heatmap (2015–21) | Custom HTML grid | ✅ By month + year |
| Movie Runtime Breakdown | Donut | 5 runtime buckets |
| TV Show Seasons | Bar | Season distribution |

### Cross-Filter Engine
- Click **any chart** → all others update from real 8,807-record dataset
- **Toggle** — click same element again to deselect
- **Stack multiple filters** across charts simultaneously
- **Active filter tags** — click `×` to remove individual filters
- **"Clear filters"** button resets everything at once

### UX Improvements Over v1
- ✅ Trend chart click is now **wired** (was broken in v1)
- ✅ `chart.update()` used instead of destroy+recreate — **no more flash**
- ✅ Genre bar shows **Movie vs TV Show split** in each bar
- ✅ **YoY Growth Rate** chart added (was missing)
- ✅ **Bubble/Scatter** chart: duration vs release year
- ✅ **Heatmap**: monthly content additions 2015–2021
- ✅ **2019 peak annotation** on trend chart
- ✅ **Change summary bar** — "Showing X of 8,807 filtered out"
- ✅ **Export CSV** of currently filtered data
- ✅ **Mobile responsive** (collapses below 900px)
- ✅ Sidebar and chart click filters stay **in sync**

---

## 📊 Key Insights

| Insight | Detail |
|---------|--------|
| 🇺🇸 USA dominates | 3,689 titles — 41.9% of library |
| 📈 2019 was peak year | 1,999 titles added |
| 📉 2020–21 decline | COVID production slowdown |
| 🎬 Movies outnumber TV 2.3:1 | 6,131 vs 2,676 |
| 🚀 2016 explosion | +472.6% YoY as Netflix went global |
| 🌏 India is #2 | 1,046+ titles |
| ⏱ Sweet spot: 90–120 min | Most common movie runtime |
| 📺 Most shows: 1 season | 1,793 of 2,676 TV shows |

---

## 🗂️ Repository Structure

```
netflix-dashboard/
├── netflix_dashboard.html   ← Open this in any browser
├── netflix.csv              ← Source dataset
├── README.md                ← This file
├── .gitignore
└── LICENSE
```

---

## 🚀 Getting Started

### Run Locally
```bash
git clone https://github.com/YOUR_USERNAME/netflix-dashboard.git
cd netflix-dashboard
open netflix_dashboard.html        # macOS
start netflix_dashboard.html       # Windows
xdg-open netflix_dashboard.html   # Linux
```

### Push to GitHub
```bash
git init
git add .
git commit -m "feat: Netflix analytics dashboard with cross-filtering"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/netflix-dashboard.git
git push -u origin main
```

### Enable GitHub Pages
1. Go to **Settings → Pages**
2. Source: `main` branch → `/ (root)` → **Save**
3. Live at: `https://YOUR_USERNAME.github.io/netflix-dashboard/netflix_dashboard.html`

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| Chart.js 4.4.1 | All chart visualizations |
| chartjs-plugin-annotation 3.0.1 | Peak year annotation |
| Inter + Bebas Neue (Google Fonts) | Typography |
| Vanilla JS (ES2020) | Filter engine & state |
| HTML5 / CSS3 | Layout, heatmap, country bars |

**Zero npm · Zero build step · Zero server · Opens in any browser**

---

## 🏗️ How It Works

```
Embedded Data (312KB JSON)
  8,807 records: [type, ratingIdx, yearAdded, releaseYear,
                  month, genreIdxs[], countryIdxs[], extra]

State (SEL object)
  Sidebar: type, rating, country, yearFrom, yearTo
  Chart clicks: clickType, clickRating, clickCountry,
                clickGenre, clickReleaseYear, clickYearAdded, clickHeatCell

Filter Engine
  computeVisible() → O(n) single pass → visIds[]
  aggregate(visIds) → counts all dimensions in one loop

Render
  10 chart builders consume agg{}
  chart.update('active') → smooth animated transitions (no flash)
```

---

## 📁 Dataset

**Source:** [Netflix Movies and TV Shows — Kaggle](https://www.kaggle.com/datasets/shivamb/netflix-shows)  
8,807 titles · 127 countries · 42 genres · Data through 2021  
Embedded as compact JSON directly in the HTML — no API calls needed.

---

## 📄 License

MIT — see [LICENSE](LICENSE)

---

*Built with Chart.js · Self-contained · No build tools required*
