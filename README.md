# Manufacturing Financial Year-End Close | ELT | Financial Analysis | Executive Dashboard | Excel
---

## Executive Summary

A mid-sized kitchen appliance manufacturer needed a structured year-end financial close across fragmented ERP, MES, and Finance data with no unified reporting layer. I performed a full ELT pipeline in Excel — loading 22,000+ raw records across 12 tables, cleaning and transforming the data using Power Query, building a complete financial analysis layer, and delivering an interactive executive dashboard. Next steps include automating the refresh cycle and expanding into variance analysis against budget. The result: a single source of truth revealing **$78M in revenue, 56.1% gross margin, and $23.7M net profit** for FY2024.

---

## Business Problem

At year-end, finance teams in mid-sized manufacturers face a recurring challenge: data lives across multiple systems — ERP, MES, warehouse management, and the general ledger — with no single consolidated view of financial performance. Manual reconciliation is error-prone, time-consuming, and leaves leadership without a reliable picture of profitability until weeks after close.

Existing approaches fail because raw exports contain duplicates, inconsistent formats, missing values, and no standardised structure — making pivot tables and dashboards built directly on raw data unreliable.

**This analysis was designed to answer:**
1. Did the business hit its revenue target, and which products and segments drove performance?
2. What is the true gross margin and net profit after accounting for actual production costs and operating expenses?
3. Where are the highest-margin opportunities in the product portfolio?

---

## Methodology

**Microsoft Excel + Power Query**
All 12 raw CSV files were loaded as-is into Excel, preserving raw data integrity before any transformation. Power Query was used for the full transformation layer — removing duplicates, standardising date formats across 5 variants, filling and recalculating null values, stripping currency suffixes, and merging tables to derive calculated fields such as Profit (Revenue − Quantity × ActualCost) and QuantityAvailable (OnHand − Reserved).

**Financial Analysis Layer**
Pivot tables were built on clean data to produce revenue by product and segment, COGS breakdown, gross margin analysis, OpEx review, inventory valuation, and a year-end profitability summary — covering every dimension required for a formal financial close.

**Executive Dashboard**
An interactive dark-theme dashboard was designed directly in Excel using chart objects, KPI cards with sparklines, a gauge chart, and narrative storytelling cards — built for leadership consumption without requiring any external BI tool.

---

## Specific Skills

| Tool | Technical Techniques |
|---|---|
| **Power Query (M)** | Table.Distinct for deduplication, Date.From for multi-format date parsing, Table.NestedJoin for cross-table merges, Table.ReplaceValue for null handling, Text.Proper for categorical standardisation, custom column formulas, promoted headers, changed data types |
| **Excel** | Pivot tables, calculated fields, slicers, sparklines, gauge charts, donut charts, line charts, KPI card design, conditional formatting, cross-sheet cell referencing |
| **ELT Process** | Raw data preservation, transformation sequencing, data quality auditing, referential integrity checks, multi-table join logic |
| **Financial Analysis** | COGS derivation, gross margin calculation, net profit reconciliation, OpEx classification, inventory valuation, revenue per unit, COGS ratio |

---

## Results & Business Recommendations

**1. Refrigerator French Door is the single biggest revenue driver — double down.**
At 18.6% of total revenue ($14.5M) and the highest absolute gross profit ($7.9M), this product line deserves priority investment in inventory, marketing, and retail placement.

**2. Toasters and Coffee Makers have the strongest margins — scale them.**
Gross margins of 60–63% on small appliances significantly outperform large appliances (~55%). Growing this segment would improve overall portfolio profitability without increasing COGS proportionally.

**3. Retailer concentration is a risk — diversify the channel mix.**
73% of revenue ($56.9M) comes from just 11 retailers. A single lost account could materially impact the top line. E-Commerce at 13.5% represents the highest-growth opportunity to reduce this dependency.

**4. OpEx is lean at 25.7% of revenue — monitor for underinvestment.**
$20M in operating expenses across Utilities, Marketing, Depreciation, Admin, and Logistics is efficient, but below industry average for manufacturers (35–45%). This warrants a review to ensure cost discipline isn't limiting growth capacity.

**5. Revenue target gap is closable — $90M is achievable in FY2025.**
At $78M against a $90M target (87% achievement), a 15% growth trajectory is realistic given stable margins, a loyal retailer base, and an untapped small appliance growth opportunity.

<img width="1476" height="880" alt="Screenshot 2026-05-06 233730" src="https://github.com/user-attachments/assets/876055ee-901c-4094-be12-80cb40677774" />


---

## Next Steps

- **Budget vs Actual variance analysis** — compare FY2024 actuals against planned budget by product and department to identify where the business over or underperformed
- **Automated refresh pipeline** — connect Power Query directly to source system exports so the dashboard refreshes with one click at each month-end close
- **Customer-level profitability** — extend the analysis to calculate net margin per customer, accounting for discounts and logistics costs, to identify the most and least profitable accounts
- **FY2025 forecasting model** — build a forward-looking revenue and margin forecast using FY2024 as the baseline
- **Limitations** — this analysis is based on simulated data; real-world application would require validated GL account mappings, confirmed FX rates for multi-currency transactions, and audited inventory valuations

---

*Repo includes: Excel workbook with all 12 tables, financial analysis sheet, and executive dashboard.*
