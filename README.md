# 🌿 Plant Company Performance Dashboard - Power BI

> **When sales are declining, which markets do you fix first, and how do you know?**
> This dashboard gives leadership the answer in under 60 seconds.


## 💼 The Business Problem

Performance reviews shouldn't require a data analyst in the room. Yet most companies still run on static reports that show *what happened* but not *where to focus*.

This executive dashboard was built for a global plant products company operating across multiple countries and product types (Indoor, Outdoor, Landscape). In 2023, the business was facing:

- **Sales declining $512K vs. prior year** (YTD $13.00M vs. PYTD $13.51M)
- **Gross profit down $265K vs. prior year** (YTD $5.15M vs. PYTD $5.42M)
- No clear visibility into *which markets* were dragging performance
- No single view connecting volume, revenue, and profitability

Leadership needed to know: where to cut losses, where to double down, and which accounts were worth protecting.

## 📊 The Numbers at a Glance (2023)

| Metric | YTD | PYTD | Variance |
|---|---|---|---|
| **Sales** | $13.00M | $13.51M | **-$512.26K** 🔴 |
| **Gross Profit** | $5.15M | $5.42M | **-$265.29K** 🔴 |
| **Quantity** | 555.66K units | 538.61K units | **+17.05K** 🟢 |
| **GP%** | 39.62% | — | — |

> Volume is actually *up* (+17K units), but both revenue and profit are down, signalling a pricing or mix problem worth investigating.

## 📐 What I Built

A multi-page interactive Power BI dashboard across three performance dimensions, each answering a distinct business question.

### Page 1: Gross Profit Performance
*"Are we making money, and where are we losing it?"*

**Key Numbers:**
- YTD Gross Profit: **$5.15M** vs. PYTD **$5.42M** → **-$265.29K**
- GP%: **39.62%**
- Biggest single-country drag: **China at -$405K**

**Visuals:**
- **KPI cards** - YTD, PYTD, variance, and GP% at a glance
- **Bottom 10 Countries Treemap** - China dominates the underperformance, followed by Sweden (-$63K), United States (-$57K), Norway (-$52K)
- **Waterfall Chart** -  Month-by-month gross profit variance vs. prior year; June/July showed recovery (+$90K, +$70K) before a sharp drop in Oct/Nov (-$150K, -$40K)
- **Trend lines by Product Type** - Indoor, Outdoor, Landscape performance vs. PYTD across all 12 months
- **Scatter (GP% vs. Account Value)** - Segments accounts by margin quality; highlights high-revenue but low-margin accounts below the 40% GP threshold

### Page 2: Quantity Performance
*"Is demand up or down, and which products and markets are driving it?"*

**Key Numbers:**
- YTD Quantity: **555.66K units** vs. PYTD **538.61K** → **+17.05K** ✅
- Biggest volume drags: **China (-9.76K)**, **France (-9.36K)**, **Sweden (-6.71K)**

**Visuals:**
- Volume KPIs with prior year comparison
- **Waterfall Chart** - May/June/July drove the gains (+12K, +13K, +6K); partially offset by dips in Aug/Oct
- **Monthly trend by product type** - Volume peaking in March/April (~52K) and November (~51K)
- **Scatter (GP% vs. Quantity)** - Identifies high-volume accounts with thin margins

### Page 3: Sales Performance
*"Where is revenue growth coming from, and what's stalling?"*

**Key Numbers:**
- YTD Sales: **$13.00M** vs. PYTD **$13.51M** → **-$512.26K**
- Biggest country revenue decline: **China at -$760K**
- Other significant declines: Sweden (-$240K), France (-$150K), Poland (-$112K), Netherlands (-$97K)

**Visuals:**
- Revenue KPIs with prior year comparison
- **Bottom 10 Treemap** - China accounts for the majority of the sales shortfall
- **Waterfall Chart** - June/July positive swing (+$230K, +$200K) followed by a steep Nov decline (-$230K)
- **Scatter (GP% vs. Sales Value)** -  Maps revenue concentration against profitability to identify strategic accounts


## 🔍 Key Business Insights

**1. Volume is growing, but revenue and profit are falling**
The company shipped 17K more units in 2023 than the prior year, yet lost $512K in revenue and $265K in gross profit. This suggests a mix shift toward lower-priced or lower-margin products,  a pricing strategy question that needs attention.

**2. China is a critical risk market**
China is the #1 drag across all three dimensions: -$760K in sales, -$405K in gross profit, and -9.76K in volume. This is not a seasonal blip, it requires a dedicated market review.

**3. Mid-year recovery didn't hold**
June and July showed strong positive momentum in both sales and gross profit vs. the prior year, but October–November reversed those gains sharply. Understanding what drove the mid-year improvement could unlock a repeatable strategy.

**4. Most accounts cluster below the 40% GP threshold**
The account segmentation scatter shows that the majority of accounts are concentrated in the 30–45% GP range. There are outliers with high GP% but low volume potential candidates for targeted growth investment.


## 🎨 Design Decisions

**Why a waterfall chart for monthly variance?**
A waterfall shows both direction and magnitude simultaneously. A manager can instantly see that July was a $230K improvement over the prior year, partially offset by an April dip, without reading two separate numbers in a table.

**Why treemap for the bottom countries?**
Size equals the magnitude of underperformance. China's dominance is visually undeniable;  it draws the eye to the biggest problem first rather than burying it in a sorted list.

**Why scatter for GP% vs. value?**
Revenue and profitability don't always move together. The scatter forces the conversation about which accounts are actually worth protecting vs. which are high-revenue but margin-dilutive.


## 🛠 Tools & Technologies

`Power BI Desktop` · `DAX` · `Data Modeling` · `Interactive Slicers & Filters`

**Key DAX Measures Built:**
- `YTD Sales / Gross Profit / Quantity` - cumulative from Jan 1 to selected date
- `PYTD Sales / Gross Profit / Quantity` - same period prior year
- `YTD vs PYTD` - absolute variance
- `GP%` - gross profit margin at account and aggregate level

## 📸 Dashboard Previews

### Gross Profit Performance
<img width="1456" height="821" alt="image" src="https://github.com/user-attachments/assets/d76d2ffd-370a-4105-ba08-fa6faceb6e62" />

### Quantity Performance
<img width="1456" height="826" alt="image" src="https://github.com/user-attachments/assets/2d2cd7fa-74bf-4100-8063-766ba7de082b" />

### Sales Performance
<img width="1456" height="829" alt="image" src="https://github.com/user-attachments/assets/c008cf45-33fe-48ca-916d-0666c9452eae" />


## 📁 Files in This Repo

| File | Description |
|---|---|
| `Plant_DTS.xlsx` | Source data used to build the dashboard |
| `Performance Rate.pbix` | Interactive Power BI report, download to explore live filters, slicers, and full DAX measures across all 3 dashboard pages |
