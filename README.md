# Premier League Financial & Performance Dashboard

*An interactive Tableau dashboard integrating club finances with on-pitch performance across three Premier League seasons (2021/22–2023/24) to measure how efficiently clubs convert money into results.*

🔗 **[View the live dashboard on Tableau Public](https://public.tableau.com/app/profile/arron.singh/viz/PremierLeagueDashboard_17559526465020/PremierLeagueFinancialPerformanceDashboard)**


---

## Overview

Financial strength doesn't always translate into on-pitch success. Clubs spend heavily on wages and transfers, yet results vary widely. Financial figures and performance stats are widely available — but rarely brought together in one place where you can compare clubs on **efficiency**, not just spend.

This project asks: **which clubs get the most performance per pound, and which spend heavily for little return?**

## Data

- **Scope:** 20 clubs per season across three seasons (60 club-season records).
- **Sources:** Transfermarkt and official club financial accounts for financial data; official league statistics for performance data.
- **Note on quality:** Smaller clubs disclose less detail, so a small number of figures are estimates cross-checked against secondary sources. This is flagged in the report rather than hidden — see Limitations.

## Process

1. **Excel** — compiled and structured the raw dataset; built calculated metrics (net spend, revenue per point, etc.). The dataset went through five iterations as scope and metrics expanded.
2. **MySQL** — validated data integrity: removed duplicates, handled nulls and missing values, corrected data types, standardised club/season naming.
3. **Tableau** — built the interactive two-page dashboard.

## KPIs

Eleven financial and performance KPIs were designed to make clubs with very different budgets directly comparable. The key efficiency metrics:

| KPI | Formula | What it shows |
|---|---|---|
| Cost per Point | Wages ÷ League Points | Cost of each point earned |
| Wins per Wage | Wins ÷ Total Wages | Wins returned per pound of wages |
| Net Spend per Point | Net Transfer Spend ÷ Points | Transfer-market efficiency |
| Wage-to-Revenue Ratio | Wages ÷ Revenue × 100 | Financial sustainability |
| Revenue per Point | Revenue ÷ Points | Revenue efficiency vs output |

## The Dashboard
<img width="1299" height="1299" alt="Premier League Financial   Performance Dashboard " src="https://github.com/user-attachments/assets/dc5356a4-eb8b-4410-8642-f20b34264bf2" />

**Page 1 — Main dashboard:** KPI tiles plus five charts, all driven by club and season filters:
- Wages vs Points (scatter)
- Net Spend vs Points (scatter)
- Cost Per Point (bar, league-wide benchmark)
- Wins Per Wage (bar, league-wide benchmark)
- Revenue by League Position (line)

<img width="1249" height="1259" alt="DataSet" src="https://github.com/user-attachments/assets/360a7574-c48c-4798-8e8c-466aba966ca0" />

**Page 2 — Data view:** the full filterable, searchable dataset for transparency and deeper inspection.

## Key Findings

- **High spend broadly correlates with success** — Manchester City and Liverpool sit at the top on both wages and points.
- **Efficient over-performers exist** — Brighton and Brentford deliver strong returns on far smaller budgets.
- **Spending power doesn't guarantee efficiency** — Chelsea and Manchester United posted high costs per point relative to results.
- **Revenue rises with league position**, driven by broadcasting and competition income — but brand and stadium size create outliers (e.g. Everton's revenue relative to finish).

## Limitations

- Club-season level data only — no player-level granularity, so a single marquee signing can distort net-spend efficiency.
- Some smaller-club figures are estimates.
- Single league, three seasons — findings don't generalise to other competitions.
- Exploratory, not predictive — no forecasting.

## Full Report

The complete dissertation, including literature review, methodology and evaluation, is in the `report` folder.
