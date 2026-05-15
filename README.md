# Coffee Sales Performance Dashboard
## A comprehensive Power BI report analyzing sales trends, and product performance for a retail coffee chain.

## Live Preview 
[**Click here to view the live interactive report**](https://app.powerbi.com/groups/me/reports/0337d62d-f611-4640-825f-b04366bff1b1/733ff9d40d5ae48c9cb0?experience=power-bi)

## Key Business Questions Addressed
Product Optimization: Which coffee blends contribute to 80% of the revenue (Pareto Analysis)?

Temporal Trends: Are there specific "rush hours" or seasonal dips in sales?

Regional Growth: Which store locations are underperforming relative to their local targets?

## Data Transformation (Power Query)
Cleaning: Handled nulls in "Customer Loyalty" data and standardized date formats.

Modeling: Implemented a Star Schema with a dedicated Dim_Date table for time-intelligence functions.

Currency Conversion: Automated daily exchange rate updates for international store locations.

## DAX Highlights
Total Revenue: The foundation of the report, calculating gross sales across all products.

Total Transactions: Tracks volume to identify high-traffic periods.

Average Transaction Value (ATV): A critical efficiency metric calculated as:

Average Transaction = DIVIDE([Total Revenue], [Total Transactions], 0)

Revenue Last Month: Utilizes time-intelligence to allow for month-over-month (MoM) growth comparisons:

Revenue LM = CALCULATE([Total Revenue], DATEADD('Date'[Date], -1, MONTH))

## How to Use
Download the Coffee_Sales_Report.pbix file.

Open in Power BI Desktop.

