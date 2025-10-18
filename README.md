# Financial Performance Dashboard

## Project Overview
This project presents an interactive **Financial Performance Dashboard** built in **Power BI** for monitoring the company’s financial health on a monthly basis.  
The dashboard provides insights into revenue, profitability, cash flow, and working capital efficiency, enabling management to make data-driven decisions.

## Objective
To design and deliver a **monthly-level interactive dashboard** that visualizes the company's key financial KPIs, including Revenue, Gross Margin %, EBITDA %, and Net Cash, with the ability to filter by date, region, and product/service.


## Key Insights
- **Revenue Growth:** Consistent month-over-month increase, peaking in December.  
- **Profitability:** Gross Margin at **45.55%**, EBITDA Margin at **24.81%**, indicating strong cost control.  
- **Cash Flow:** Net Cash position steadily improves each month, reflecting efficient cash management.  
- **Regional Performance:** The **South region** leads slightly, while **East** shows scope for improvement.  
- **Receivables Aging:** Averages around **30 days**, aligned with standard credit terms.  
- **Payables Aging:** Appears unusually high and requires data validation.  
- **Budget Alignment:** Actual revenue closely matches budget targets, with small positive variances in key months.

## Dataset Information
**Dataset Name:** `Data`  
**Columns Included:**
Month | Region | Product/Service | Revenue | COGS | Gross Profit | Opex | EBITDA | Cash Inflows | Cash Outflows | Receivables Aging (Days) | Payables Aging (Days) | Revenue Budget | Budget Variance %

## ⚙️ DAX Measures Used
- **Total Revenue:** `SUM(Data[Revenue])`
- **Total COGS:** `SUM(Data[COGS])`
- **Gross Profit:** `SUM(Data[Gross Profit])`
- **Gross Margin %:** `DIVIDE([Gross Profit], [Revenue])`
- **EBITDA %:** `DIVIDE([EBITDA], [Revenue])`
- **Net Cash:** `SUM(Data[Cash Inflows]) - SUM(Data[Cash Outflows])`
- **Revenue YTD:** `TOTALYTD([Revenue], 'Data'[Month])`
- **Revenue MoM %:** `( [Current Month Revenue] - [Previous Month Revenue] ) / [Previous Month Revenue]`

## 📈 Dashboard Features
### KPI Cards
- Revenue  
- Net Cash  
- Gross Margin %  
- EBITDA %  
- Revenue YTD  
- Revenue MoM %

### Visuals Included
1. **Revenue and Gross Profit by Month** – Combo chart showing monthly trend.  
2. **Revenue by Product/Service** – Horizontal bar chart highlighting top-performing offerings.  
3. **Revenue vs Budget and Variance %** – Budget comparison by month.  
4. **Net Cash Movement** – Waterfall chart showing monthly inflow and outflow impact.  
5. **Revenue by Region** – Donut chart showing regional contribution.  
6. **Average Receivables Aging by Month** – Horizontal bar chart.  
7. **Total Payables Aging by Month** – Horizontal bar chart.

### Interactivity
- Filters for **Region**, **Product/Service**, and **Date Range**
- Drill-down capability from month to product/service level
- Dynamic KPI cards responding to slicer selections

## Design Theme
- **Layout:**  
  - Top section: KPI summary  
  - Middle section: Revenue and Profit analysis  
  - Bottom section: Cash Flow and Working Capital insights  

## Data Cleaning & Preparation
- Validated numerical consistency across revenue, cost, and cash columns.  
- Checked for missing or inconsistent entries in aging data.  
- Ensured all months are properly ordered for trend analysis.  
- Adjusted incorrect budget variance calculations.

## Outcome
The dashboard enables financial stakeholders to:
- Monitor monthly and year-to-date performance.  
- Track budget adherence and variance.  
- Assess profitability across products and regions.  
- Evaluate liquidity and working capital efficiency.  

## Deliverables
- **Power BI File:** `Financial_Performance_Dashboard.pbix`  
- **Insights Report:** `Financial_Insights_Report.pdf`  
- **README File:** (this document)

## Tools Used
- **Power BI** – Data visualization and dashboard design  
- **Excel** – Data cleaning and preparation  
- **DAX** – Calculations for KPIs and metrics  

## Author
**Lopita Mishra**  
