# Walmart Sales Analysis

**Intern ID:** CITS8439 | **Author:** Nithyashree S
End-to-end analysis of Walmart weekly sales across 45 stores: Excel cleaning, Python EDA, and a Power BI dashboard.

## Goal
Understand what drives weekly sales (time, holidays, weather, economy, store).

## Dataset
- 6,435 rows × 8 columns, weekly sales per store, Feb 2010 to Oct 2012
- Columns: Store, Date, Weekly_Sales, Holiday_Flag, Temperature, Fuel_Price, CPI, Unemployment

## Tools
Excel (cleaning) → Python: pandas, matplotlib, seaborn (EDA) → Power BI (dashboard)

## Data cleaning (Excel)
- 6,435 data rows, 8 columns
- 0 blank cells, 0 duplicate rows
- All dates verified and standardised to yyyy-mm-dd
- Exported as CSV UTF-8 (`Walmart.csv`)

## Dashboard
![Walmart Sales Dashboard](Sales%20trend%20visualization%20project/dashboard.png)

Interactive Power BI dashboard built from the cleaned data.
- **KPI cards:** total sales, average weekly sales, store count, holiday lift %
- **Charts:** weekly sales trend, average sales by month, top 10 stores, holiday vs non-holiday weeks
- **Filters:** Year, Holiday Type and Store; clicking any chart cross-filters the rest
- **Key insights box:** summary of the main findings

## Key findings
1. Data is clean: 0 missing values and 0 duplicates.
2. Sales peak in December, and 8 of the top 10 sales weeks are in Nov or Dec.
3. The two biggest weeks are just before Christmas and are not flagged as holidays.
4. Holiday-flagged weeks have only slightly higher median sales than normal weeks (about 8% higher on average).
5. Temperature, fuel price, CPI and unemployment show weak correlation with weekly sales.
6. There are 34 outliers, all in Nov and Dec. They are real peak-season sales, so they were kept.
7. Store matters most: the top store sells about 8x the bottom store.

## Recommendations
- Plan stock and staffing around the pre-Christmas and Thanksgiving weeks.
- Use a custom "Peak Season" label instead of relying only on Holiday_Flag.
- Review the lowest-performing stores (33, 44, 5).

## Limitations
- Data covers Feb 2010 to Oct 2012, so Nov, Dec and Jan have only 2 years of data.
- Correlation does not show cause.

## Files
All files are in the `Sales trend visualization project` folder:
- `Sales Trend Visualization.ipynb`: analysis notebook
- `Walmart.csv`: cleaned dataset
- `Walmart.xlsx`: Excel cleaning workbook
- `Walmart_Sales_Dashboard.pbix`: Power BI dashboard (open with Power BI Desktop)
- `dashboard.png`: dashboard screenshot

