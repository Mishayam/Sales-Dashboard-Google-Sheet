# Sales Dashboard (Google Sheets)

A Google Sheets sales dashboard built from a messy, synthetic sales dataset — covering data cleaning, imputation, validation, and an interactive dashboard with slicers.

**Note:** Source data was synthetically generated to simulate realistic messy sales records (not real business data).

## Data Cleaning Steps

- Trimmed whitespace and fixed inconsistent casing (e.g. "north" / "SOUTH" / " East" → standardized)
- Standardized inconsistent date formats
- Removed exact duplicate rows
- Stripped inconsistent currency symbols from price fields
- Validated column data types (decimal for price, text for text fields)

## Imputation Methodology

- **Missing Units Sold or Unit Price**: filled using the average value for that product category from other rows
- **Missing both Units Sold and Unit Price**: row deleted (not enough information to reliably impute)
- **Missing Sales Rep name**: filled with placeholder value `"Admin"`

This logic is documented here for transparency — imputed/placeholder values are not original source data.

## Dashboard Features

- Slicers: Sales Rep, Product Category, Region
- KPI cards: Total Revenue, Total Orders
- Charts:
  - Sales Rep Performance (units sold by rep)
  - Units Sold share by Product Category (pie)
  - Region Revenue & Productd Sold (dual-axis bar — separate axes since the two metrics differ in scale)
  - Region vs Product Category (clustered bar)

## Skills Demonstrated

- Data cleaning: whitespace, casing, date standardization, deduplication
- Defensible imputation strategy (category-average fill, row-drop threshold, placeholder labeling)
- Data validation (type restrictions)
- Dashboard design: slicers, KPI cards, dual-axis charts, avoiding misleading chart types (log scale, trend lines on categorical data)

## Companion Project

See the Excel version of a project for the same workflow built with Excel formulas (SUM, IF, COUNTIF, SUMIF, INDEX/MATCH, VLOOKUP).


