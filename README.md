# 🎬 Movie Box Office Analytics — Excel Dashboard

An end-to-end data analytics project built entirely in **Microsoft Excel**: raw data cleaning, a formula-driven pivot-table calculation layer, and an interactive, cinema-themed dashboard with KPI cards and charts.

![Excel](https://img.shields.io/badge/Excel-217346?style=flat&logo=microsoft-excel&logoColor=white)
![Status](https://img.shields.io/badge/status-complete-brightgreen)

## 📊 Overview

This project simulates a real-world analyst workflow: take a messy movie box-office export, clean it, and turn it into a decision-ready dashboard.

- **222 cleaned movie records** (from 238 raw records)
- **555 live formulas** — nothing is hard-coded, the whole workbook recalculates if the data changes
- **Fields:** Movie Title, Genre, Director, Release Year, Budget, Revenue, IMDb Rating, Runtime, Language, Production Company, Country

## 📁 Workbook Structure

| Sheet | Purpose |
|---|---|
| **Dashboard** | KPI cards + 6 charts — the main interactive view |
| **Pivot Tables** | SUMIFS / COUNTIFS / AVERAGEIFS summary tables that feed every chart |
| **Cleaned Data** | Final dataset as a native Excel Table, with conditional formatting |
| **Raw Data** | Original unprocessed export (duplicates & blanks kept for comparison) |
| **Read Me** | Project walkthrough and interview talking points |

## 🧹 Data Cleaning

- Removed **16 duplicate** records (composite key: Title + Year + Director, case-insensitive)
- Imputed missing numeric values (Budget, Revenue, IMDb Rating, Runtime) using **genre-level medians**
- Filled missing categorical fields (Director, Language, Production Company, Country) with `"Unknown"`
- Standardized text casing, trimmed whitespace, converted currency-formatted text back to numbers
- Added derived fields: **Profit** (Revenue − Budget) and **ROI %**

## 📈 Dashboard Components

**KPI Cards:** Total Movies · Total Revenue · Average IMDb Rating · Average Runtime · Number of Genres

**Charts:**
- Revenue by Release Year (line)
- Top 10 Highest-Grossing Movies (bar)
- Genre Distribution (pie)
- Top 10 Directors by Revenue (bar)
- Language Distribution (pie)
- IMDb Rating Distribution by Band (column)

**Formatting:** color-scale on IMDb Rating, data bars on Budget/Revenue, red highlighting on loss-making titles.

## 🎨 Design

Dark, cinema-inspired theme — navy background with IMDb-gold accents — so the dashboard reads like a studio analytics tool rather than a generic spreadsheet.

## 🚀 Getting Started

1. Download [`Movie_Box_Office_Analytics.xlsx`](./Movie_Box_Office_Analytics.xlsx)
2. Open in Excel (formulas require Excel 2010+ for full compatibility)
3. Use the filter buttons on the **Cleaned Data** table to slice by Genre, Year, or Language
4. To add true clickable **Slicers**: select any cell in Cleaned Data → `Insert > PivotTable` → `Insert > Slicer` on Genre / Release Year / Language

## 🗂️ Data Note

The dataset is a synthetically generated, illustrative sample (fictional titles/directors) built to mirror the shape of a real box-office dataset — swap in real data by pasting into **Raw Data** and re-applying the same cleaning logic.

## 🛠️ Tech

Built with Microsoft Excel — formulas (`SUMIFS`, `COUNTIFS`, `AVERAGEIFS`, `INDEX`/`MATCH`, `LARGE`), native Excel Tables, PivotChart-style native charts, and conditional formatting. No add-ins or macros required.

## 📄 License

Feel free to fork, adapt, and reuse for learning or portfolio purposes.
