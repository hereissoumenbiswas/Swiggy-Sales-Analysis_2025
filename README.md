# 🍔 Swiggy Sales Analysis — Pan-India Business Performance (Jan–Aug 2025)

An end-to-end Excel analytics project built from a client Business Requirement Document (BRD/SOW), covering data cleaning, pivot-based analysis, and an executive dashboard for a nationwide Swiggy order dataset.

## 📌 Project Overview

**Objective** | Give business stakeholders a clear view of platform health (sales, ratings, orders) and uncover operational patterns to guide staffing, promotions, and regional strategy |
| **Data Period** | January 2025 – August 2025 |
| **Scope** | Pan-India (28 states/UTs, 28 cities, 993 restaurants) |
| **Order Volume** | 1,97,430 orders |
| **Tools Used** | Microsoft Excel (Power Pivot, PivotTables, PivotCharts, Dashboard) |

---

## 🎯 Business Problem

The client's BRD asked for two layers of analysis:

**1. Executive KPIs** — a high-level snapshot of business health: Total Sales, Average Rating, Average Order Value (AOV), Rating Count, and Total Orders.

**2. Operational Deep-Dive** — root-cause and trend analysis to support day-to-day decisions:
- Monthly sales trend → plan courier manpower and discount timing
- Daily sales trend (Sun–Sat) → identify peak demand days
- Weekly sales trend → spot peak operational periods across the year
- Veg vs Non-Veg sales split
- State-wise sales (geo view)
- Quarterly summary (Sales, Ratings, Orders)
- Top 5 cities by sales

---

## 🧹 Data Preparation

- Started from raw transactional data (State, City, Order Date, Restaurant, Dish, Price, Rating, Rating Count).
- Built a clean layer adding calculated fields: **Day of week, Quarter, Week number, and Food Type (Veg/Non-Veg)**, derived from the dish category — this is what unlocked the daily/weekly/food-type analysis the BRD asked for.
- Fed the clean table into PivotTables to produce every metric the client requested, then wired those pivots into a single-page Dashboard.

---

## 📊 Executive KPIs

| Metric | Value |
|---|---|
| **Total Sales** | ₹5.30 Crore (₹5,30,12,505.77) |
| **Total Orders** | 1,97,430 |
| **Average Order Value (AOV)** | ₹268.51 |
| **Average Rating** | 4.34 / 5 |
| **Rating Count (engagement volume)** | 55,91,574 |

> Note: "Rating Count" is summed exactly as the BRD defines it — a platform engagement volume metric — rather than a per-transaction review count, so it shouldn't be read as "1 rating per order."

---

## 🔎 Key Insights

**1. Monthly trend is stable, not seasonal-spiky.**
Sales moved in a tight ₹6.27M–₹6.83M band every month (Jan ₹68.3L → Aug ₹67.9L), with Feb the softest month and Jan/May/Aug roughly tied for the strongest. This says the business has a steady base demand rather than one or two blockbuster months — useful for keeping courier staffing fairly constant rather than over-hiring for a "peak season" that doesn't really exist here.

**2. Saturday is the busiest day; Tuesday is the quietest.**
Daily sales across the whole 8 months: Sat ₹77.8L > Thu ₹76.6L > Fri ₹75.8L > Sun ₹76.4L > Wed ₹75.4L > Mon ₹74.5L > Tue ₹73.6L (lowest). Weekends plus Thursday clearly outperform the early week — a natural window for pushing restaurant promotions on Tuesdays to smooth demand.

**3. Veg dominates order volume, but Non-Veg drives a bigger basket.**
Veg = 69.4% of orders and 63% of revenue (₹3.34 Cr). Non-Veg = only 30.6% of orders but 37% of revenue (₹1.96 Cr). Doing the AOV split: **Non-Veg AOV is ₹325**, about **34% higher** than Veg AOV (₹243). Non-Veg is the smaller, higher-value segment — a good candidate for upsell/bundle offers to lift overall AOV.

**4. Sales are geographically concentrated.**
Bengaluru (Karnataka) alone brings in ₹54.6L — the single largest contributor, ahead of Lucknow (₹31.2L), Hyderabad (₹30.2L), Mumbai (₹30.2L), and Delhi (₹28.3L). These **top 5 cities generate ~33% of total national sales**, while smaller markets like Sikkim, Nagaland, and Mizoram each contribute under ₹6L. That's a strong argument for city-tiered strategy: defend the metro leaders, and run targeted growth pushes (not blanket campaigns) in the long tail.

**5. Service quality holds steady regardless of volume.**
Average rating is virtually identical across all quarters (Q1: 4.343, Q2: 4.340, Q3: 4.342) even as order volume moves. Quality of service isn't slipping as the platform scales — a genuinely good sign for operations.

**6. Quarterly comparison needs a caveat — Q3 in this dataset is incomplete.**
Q1 (₹1.97 Cr, 73,096 orders) and Q2 (₹1.99 Cr, 74,163 orders) each cover 3 full months. Q3 shows only ₹1.34 Cr / 50,171 orders — but that's because the data cuts off at August, so **Q3 only has July + August (2 months), not 3**. Read at face value this looks like a decline; normalized to a monthly average, Q3 (₹67.2L/month) is actually in line with Q1 (~₹65.6L/month) and Q2 (~₹66.3L/month). Flagging this kind of denominator mismatch is exactly the sort of thing that separates a surface-level dashboard from a properly analyst-reviewed one.

**7. Weekly trend shows one standout spike.**
Across 35 weeks, sales mostly sit in a ₹14.6L–₹15.7L/week band, with a clear outlier in Week 8 (mid-February) at ₹17.6L — the single highest week in the dataset. Week 1 reads unusually low (₹8.8L) simply because it's a partial calendar week, not a real dip.

---

## 💡 Business Recommendations

- **Staffing:** Prioritize courier availability for Saturdays, Thursdays, and Fridays; Tuesdays can run leaner.
- **Promotions:** Target discount pushes on Tuesdays and in the Feb–Jun window to smooth the relatively flat monthly curve.
- **AOV growth:** Bundle or cross-sell Non-Veg items to Veg-heavy customers — it's the higher-value segment on a per-order basis.
- **Regional strategy:** Protect the top 5 metro markets (33% of revenue) while running lower-cost, targeted campaigns in low-share states instead of a one-size-fits-all national push.
- **Reporting hygiene:** Always report quarterly figures alongside a monthly-average normalization when the latest quarter is incomplete, to avoid stakeholders misreading a partial period as a downturn.

---

## 🛠️ Tools & Skills Demonstrated

`Microsoft Excel` · `PivotTables & PivotCharts` · `Data Cleaning` · `Calculated/Derived Columns` · `KPI Design` · `Dashboard Design` · `Business Requirement Analysis (BRD/SOW)` · `Stakeholder Reporting`
