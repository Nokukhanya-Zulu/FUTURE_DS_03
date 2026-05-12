# Marketing Funnel & Conversion Performance Analysis

**Future Interns — Task 3 | Data Analysis Internship**

## Project Overview

Analysis of a bank marketing campaign dataset containing **41,188 customer contacts** to understand how prospects move through the marketing funnel (Visitor → Engaged Lead → Customer). The goal is to identify drop‑off points, high‑performing channels, and actionable recommendations to improve conversion rates. The findings are presented in a **3‑page interactive Power BI dashboard**.

## Tools Used

- **Python (Jupyter Notebook)**
- **Pandas / NumPy**
- **Matplotlib / Seaborn**
- **Power BI Desktop**

## Dataset

- Raw dataset: **41,188 records, 21 columns** (Bank Marketing dataset – UCI)
- Cleaned dataset: **41,188 records, 22 columns** (added `converted` and `engaged` flags)
- Overall conversion rate (Visitor → Customer): **11.27%**

## What I Did

- Loaded and inspected the raw data
- Created binary target `converted` (1 if subscribed, else 0)
- Engineered `engaged` flag – middle funnel stage (previous campaign success or call duration above median)
- Calculated funnel metrics: conversion rates, drop‑off percentages
- Performed segment analysis: by contact method, job, month, previous outcome
- Built a **3‑page Power BI dashboard**

## Dashboard Pages

- **Page 1 – Funnel Overview**  
  Funnel chart (Visitor → Engaged → Customer), overall conversion rate (11.27%), engaged rate (50.70%), combo chart of monthly engaged leads vs conversions.

- **Page 2 – Channel & Audience Analysis**  
  Treemap of conversion by job, bar chart by contact method, scatter plot (age vs duration coloured by conversion), slicer by education, card for best channel.

- **Page 3 – Campaign Efficiency & Drop‑off**  
  Gauges for drop‑off rates (Visitor→Engaged: 49.30%, Engaged→Customer: 77.78%), matrix of conversion by day of week and month, 100% stacked bar by campaign number, card for average call duration of converted customers (~553 sec).

## Key Insights

- **Overall conversion rate:** 11.27% (4,640 of 41,188 contacts subscribed)
- **Engaged rate:** 50.70% – about half of contacts become engaged (previous success or long call)
- **Drop‑off from engaged to customer:** 77.78% – major leakage point
- **Best contact method:** Cellular (13.22% conversion) vs Telephone (7.69%)
- **Top jobs by conversion:** Student (28.01%), Retired (24.84%), Unemployed (16.82%)
- **Best month:** May (15.92% conversion), worst month: December (5.99%)
- **Average call duration – converted customers:** ~553 seconds (vs non‑converted ~201 seconds)
- **Campaign efficiency:** first contact has highest conversion (13.48%), drops sharply after 3 contacts

## Recommendations

1. Focus marketing budget on **cellular contact** – highest conversion.
2. Target high‑conversion job segments: students, retired, unemployed.
3. Improve lead engagement to reduce 49% visitor→engaged drop‑off (better targeting, faster follow‑up).
4. Retarget engaged leads that didn’t convert – 78% drop‑off means huge opportunity.
5. Schedule campaigns in **May–July** (peak conversion months).
6. Limit repeated campaigns – conversion drops sharply after 3 contacts.

## Files in This Repository

- `funnel_analysis.ipynb` — Python cleaning, feature engineering, and EDA notebook
- `cleaned_marketing_funnel.csv` — Exported clean dataset for Power BI (run notebook to regenerate)
- `Marketing_Funnel_Dashboard.pbix` — Power BI dashboard file
- `screenshots/` — Dashboard page screenshots

---

*This project demonstrates an end‑to‑end analytics workflow – from raw marketing data to interactive funnel dashboards and business recommendations.*
