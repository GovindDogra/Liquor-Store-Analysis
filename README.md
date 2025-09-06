# Liquor-Store-Analysis
Data-driven analysis of liquor store inventory &amp; sales using SQL, Python &amp; Power BI. Includes dashboards and insights from the PWC dataset to identify dead stock, slow movers, shelf-life issues, and stock-outs for better inventory and procurement decisions.

## Dataset Description

The dataset simulates a real-world retail scenario with multiple fact and dimension tables:

- Sales (12M+ records) → Transaction-level data with revenue, quantity, and profit.

- Beginning Inventory (beg_inv) → Inventory levels at the start of the year.

- Ending Inventory (end_inv) → Inventory levels at the end of the year.

- Purchase Price → Cost details for purchased items.

- Final Purchase → Vendor and product purchase records.

- Invoices → Store billing and transaction documentation.

## Data Pipeline & Flow

Steps:

### - Data Ingestion

  - Imported raw CSV files containing sales, inventory, and purchase data.

### - Data Cleaning & Transformation (Python – Pandas)

  - Imputed missing values using mean volume within the same price range.

  - Standardized volume formats (e.g., 750mL + 3/ → 750mL 3 Pk, Liter → 1L).

  - Reconstructed missing InventoryID by combining Store, City, and Brand.

  - Filled missing city names in ending inventory using beginning inventory data.

  - Normalized column formats (dates, numeric fields, text).

### - Data Modeling & Normalization

  - Built fact and dimension tables for Sales, Products, Vendors, Dates, and Occasions.

  - Removed redundant details from fact tables → improved performance and storage efficiency.

  - Designed a hybrid Star + Snowflake schema for optimized querying.

### - Data Warehousing (Snowflake)

  - Created schema and uploaded cleaned dataframes.

  - Enabled SQL-based ad-hoc analysis for business queries and reporting.

### - Dashboard Development (Power BI)

  - Built interactive dashboards to analyze sales, inventory, and vendor performance.

  - Added slicers/filters for store, month/year, and occasion to allow flexible exploration.


## 🚨 Inventory Analysis & Recommendations
## Key Findings

- Dead Stock: $282,183.65 locked in unsold inventory → requires liquidation.

- Low Sell-Through Items: High holding cost but low demand.

- Shelf Life Concerns: Products nearing expiry risk forced discounting.

- Stock-Outs: High-demand SKUs unavailable during peaks → lost sales.

- Vendor Gaps: No performance tracking → poor procurement decisions.

## Recommendations

- Immediate: Liquidate dead stock, stop reordering low performers, renegotiate vendor terms.

- Medium-Term: Implement inventory health dashboard, pilot new SKUs in small batches, apply ABC classification.

- Long-Term: Use demand forecasting, align stocking with seasonal events, develop vendor scorecards, and adopt data-driven procurement.

## Project Outcomes

- Built an end-to-end pipeline: ingestion → cleaning → warehousing → SQL analysis → dashboarding.

- Delivered a dynamic Power BI dashboard with actionable insights.

- Enabled data-driven decision-making for sales, inventory, and vendor management.

- Provided a strategic roadmap for reducing dead stock, improving turnover, and preventing stock-outs.
