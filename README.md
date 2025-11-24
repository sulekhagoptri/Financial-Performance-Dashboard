# Financial-Performance-Dashboard
Power BI Financial Performance Dashboard created using financial_data.csv

The Financial Performance Dashboard provides a comprehensive analysis of company-wide financial metrics such as Gross Sales, Profit, COGS, Discounts, Units Sold, and Profit Performance over time.

Data Cleaning (Power Query)

Steps performed during data preparation:

Removed $, hyphens, and invisible characters

Cleaned and trimmed all text fields

Converted numeric columns to Decimal Number type

Converted Date column to Date Type

Corrected column names (removed trailing spaces)

Ensured consistency across all fields

DAX Measures Used
Total Gross Sales = SUM(financial_data[Gross Sales])

Total Profit = SUM(financial_data[Profit])

Total Units Sold = SUM(financial_data[Units Sold])

Total COGS = SUM(financial_data[COGS])

Total Discounts = SUM(financial_data[Discounts])

Profit Margin = DIVIDE([Total Profit], [Total Gross Sales])

Gross Margin % = DIVIDE([Total Gross Sales] - [Total COGS], [Total Gross Sales])

Net Revenue = [Total Gross Sales] - [Total Discounts]

Discount Percentage = DIVIDE([Total Discounts], [Total Gross Sales])

Profit per Unit = DIVIDE([Total Profit], [Total Units Sold])

Yearly Gross Sales = CALCULATE([Total Gross Sales], VALUES(financial_data[Year]))

Yearly Profit = CALCULATE([Total Profit], VALUES(financial_data[Year]))

Dashboard Features
✔ KPI Indicators

Total Gross Sales

Total Profit

Total Units Sold

Total Discounts

Profit Margin

Gross Margin %

✔ Interactive Slicers

Segment

Product

Country

Year

✔ Visualizations

Sales by Country (Bar Chart)

Profit Trend by Year/Month (Line Chart)

Quarterly Profit (Column Chart)

Discount Band vs Product (Heatmap)

Gross Sales vs Discounts (Scatter Plot)

Conclusion

This dashboard allows users to analyze financial trends, understand product-level profitability, and assess the impact of discounts and costs on business revenue. The model supports strategic decision-making by offering a complete financial picture across time, geography, and segments.
