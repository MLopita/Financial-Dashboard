# Financial Performance Dashboard

### Project Overview
The **Financial Performance Dashboard** provides a comprehensive analysis of a company’s financial health by tracking revenue growth, profitability, cash flow, and working capital efficiency.  
It enables stakeholders to monitor monthly trends, compare performance against budgets, and evaluate product/service profitability across different regions and timeframes.

### Tools Used
- **Power BI** – Dashboard design, KPI calculation, and visualization  
- **Excel** – Data cleaning, transformation, and modeling  
- **DAX** – Custom measures for financial KPIs  
- **Power Query** – Data loading and shaping  

### 🎯 Objective
To analyze and visualize the company’s **financial performance** over time, focusing on:
- Revenue growth trends  
- Gross profit and EBITDA margins  
- Budget vs actual performance  
- Cash flow movement  
- Product/service-wise revenue distribution  
- Receivables efficiency  

### Key KPIs
| KPI | Description |
|-----|--------------|
| **Total Revenue (23.6M)** | Overall revenue generated across all products/services |
| **Net Cash (0.69M)** | Liquidity status after inflows and outflows |
| **Gross Margin % (45.55%)** | Profitability before operational expenses |
| **EBITDA % (24.81%)** | Operational efficiency indicator |
| **Revenue YTD (11.8M)** | Cumulative year-to-date revenue |
| **Revenue MoM (4.18%)** | Month-over-month revenue growth |

### Dashboard Components
| Chart Title | Type | Purpose |
|--------------|------|----------|
| **Revenue & Profit Trend Over Time** | Line Chart | Shows year-over-year revenue and profit trends |
| **Revenue vs Budget and Variance % by Month** | Clustered Column | Highlights monthly performance against budget |
| **Monthly Movement of Net Cash** | Waterfall Chart | Displays inflows and outflows contributing to net cash |
| **Revenue by Product/Service** | Horizontal Bar Chart | Identifies top-performing products and services |
| **Average Receivables Aging by Month** | Bar Chart | Tracks receivables collection efficiency across months |

### Key Insights
- **Revenue Growth:** Steady month-over-month increase with December peaking due to strong product demand.  
- **Profitability:** Gross Margin (45.55%) indicates efficient cost control; EBITDA Margin (24.81%) shows room for operational optimization.  
- **Cash Flow:** Consistent increase in net cash indicates healthy liquidity and disciplined expense management.  
- **Product Performance:** Product C and Service X are top performers; Product A and Service Y show potential for growth.  
- **Working Capital:** Receivables collected within 26–31 days, reflecting efficient cash management.  

### Recommendations
1. Optimize operational costs to improve EBITDA margins.  
2. Reinvest surplus cash into high-performing products and regions.  
3. Focus on cost control for underperforming services.  
4. Continue maintaining a 30-day receivables cycle for liquidity stability.  

### DAX Measures Used
`DAX
Total Revenue = SUM(Data[Revenue])
Net Cash = SUM(Data[Net Cash])
Gross Margin % = DIVIDE(SUM(Data[Gross Profit]), SUM(Data[Revenue])) * 100
EBITDA % = DIVIDE(SUM(Data[EBITDA]), SUM(Data[Revenue])) * 100
Revenue YTD = TOTALYTD(SUM(Data[Revenue]), Data[Date])
Revenue MoM % = 
VAR CurrentMonth = CALCULATE(SUM(Data[Revenue]), Data[Month] = MAX(Data[Month]))
VAR PrevMonth = CALCULATE(SUM(Data[Revenue]), Data[Month] = MAX(Data[Month]) - 1)
RETURN DIVIDE(CurrentMonth - PrevMonth, PrevMonth, 0)


### Project Structure
Financial_Performance_Dashboard
│
├── Financial_Performance_Dashboard.pbix
├── Financial Dashboard Insights Report.docx
└── Financial Dashboard.pdf

### Conclusion
The dashboard provides a clear, data-driven view of the company’s financial status — empowering decision-makers to track performance, optimize costs, and plan for sustainable growth. It effectively visualizes financial KPIs and delivers actionable insights into profitability, liquidity, and operational efficiency.
