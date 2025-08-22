# 📊 SuperStore Sales Dashboard — Power BI

An **interactive Power BI dashboard** built on the **SuperStore dataset**.  
It analyzes **Sales, Profit, Customers, Categories, Regions, and Delivery Time** using clean visuals and well-structured **DAX measures**.

---
## 📥 Download

**Power BI Desktop (no sign-in required):** open the `.pbix` locally.

## 🧰 What’s Inside

- **KPIs:** Total Sales, Total Profit, Distinct Customers, Avg Delivery Days  
- **Trends:** Sales & Profit by Month/Year  
- **Breakdowns:** Category / Sub-Category / Segment / Region  
- **Maps:** Profit and Sales by Region/State  
- **Interactivity:** Slicers (Year, Region, Category), Drill-downs, Tooltips  
- **Forecasting:** Extend line chart trends with confidence intervals

## 📐 Core DAX — Measures (with explanations)

### 1) Total Sales
```DAX
Total Sales = SUM ( Sales[Sales] )
Sums total sales. Used in KPIs, trends, and comparisons.

2) Total Profit
DAX
Copy
Edit
Total Profit = SUM ( Sales[Profit] )
Sums profit across selected filters. Shows overall profitability.

3) Profit Margin %
DAX
Copy
Edit
Profit Margin % = DIVIDE ( [Total Profit], [Total Sales] )
Safe division to calculate efficiency of sales → profit.

4) Distinct Customers
DAX
Copy
Edit
Distinct Customers = DISTINCTCOUNT ( Sales[Customer ID] )
Counts unique customers → tracks growth and retention.

5) Avg Delivery Days
DAX
Copy
Edit
Avg Delivery Days =
AVERAGEX (
    Sales,
    DATEDIFF ( Sales[Order Date], Sales[Ship Date], DAY )
)
Calculates average shipping performance (days between order and ship).


📊 Visuals — What & Why
Cards (KPIs): Sales, Profit, Customers, Avg Delivery → quick executive view
Line Chart: Sales trend (with YTD, MoM) → shows growth, seasonality
Clustered Column/Bar: Sales by Category/Sub-Category → compare performance
Stacked Column (optional): Sales by Segment → see proportion vs. total
Map: Sales/Profit by Region/State → highlight geographic hotspots
Slicers: Year, Region, Category → self-service exploration


Business Questions Answered
Which segments and regions drive the most revenue & profit?
Which categories underperform despite high sales?
How do sales trends change month-to-month?
What is the average delivery time, and does it vary by ship mode or region?
How do discounts affect profit margin?


🚀 Getting Started
Install Power BI Desktop
 (free).
Download .pbix from repo or Drive link.
Open in Power BI Desktop.
(Optional) Update Data source settings → point to data/ folder.
Refresh dataset (Home ➜ Refresh).


📝 Notes
Power BI Desktop: no sign-in needed.
Power BI Service (Web): requires sign-in for publishing.
For files >100 MB: host externally (Google Drive, OneDrive).


📬 Contact
📧 Email: sulemanyaqoob0309@gmail.com
⭐ If you find this project useful, please star the repository!
