# Walmart Sales Data Analysis

## Project Overview

This project analyzes Walmart's weekly sales data from February 2010 to October 2012 to uncover patterns, trends, and actionable business insights. The analysis examines sales performance across 45 stores, holiday impacts, seasonal patterns, and economic factor correlations.

## Dataset Information

| Attribute | Details |
|-----------|---------|
| Source | Walmart Sales Forecasting Dataset |
| Time Period | February 2010 - October 2012 |
| Total Records | 6,435 weekly sales records |
| Stores Analyzed | 45 stores |

### Column Description

| Column | Description |
|--------|-------------|
| Store | Store number (1-45) |
| Date | Week of sales |
| Weekly_Sales | Sales for that week |
| Holiday_Flag | 1 = Holiday week, 0 = Non-holiday |
| Temperature | Temperature on sale day |
| Fuel_Price | Regional fuel cost |
| CPI | Consumer Price Index |
| Unemployment | Regional unemployment rate |

## Project Structure
walmart_sales_analysis/
│
├── data/
│ └── Walmart_Sales.csv # Raw data file
│
├── outputs/
│ └── walmart_cleaned.csv # Cleaned and feature-engineered data
│ └── walmart_analysis_summary.csv # Summary metrics and KPIs
│
├── reports/
│ └── walmart_analysis_report.pdf # Professional PDF report
│
├── charts/
│ └── sales_trend.png # Sales trend over time chart
│ └── top_stores.png # Top 10 stores bar chart
│ └── holiday_effect.png # Holiday vs non-holiday comparison
│ └── monthly_pattern.png # Monthly sales pattern chart
│ └── correlation_heatmap.png # Correlation heatmap
│ └── temp_vs_sales.png # Temperature vs sales scatter plot
│
├── walmart_sales_analysis.ipynb # Main Jupyter notebook
│
└── README.md # Project documentation

text

## Key Findings

### Overall Sales Metrics

| Metric | Value |
|--------|-------|
| Total Sales (All Time) | $6.74 Billion |
| Average Weekly Sales | $1.05 Million |
| Median Weekly Sales | $0.96 Million |
| Maximum Weekly Sales | $3.82 Million |
| Minimum Weekly Sales | $0.21 Million |

### Store Performance

| Category | Store | Total Sales |
|----------|-------|-------------|
| Top Store | Store 20 | $301.4 Million |
| 2nd Best | Store 4 | $299.5 Million |
| 3rd Best | Store 14 | $289.0 Million |
| Bottom Store | Store 33 | $37.2 Million |
| Sales Gap (Best vs Worst) | 8.1x | - |

**Concentration Metrics:**
- Top 3 stores contribute: 13.2% of total sales
- Top 5 stores contribute: 21.5% of total sales
- Top 10 stores contribute: 39.1% of total sales

### Holiday Impact

| Metric | Value |
|--------|-------|
| Holiday Weeks | 450 (7.0% of total) |
| Average Sales - Holiday | $1,122,888 |
| Average Sales - Non-Holiday | $1,041,256 |
| Holiday Sales Lift | +7.8% |
| Best Holiday Week | Nov 25, 2011 (Store 4: $3.0M) |
| Highest Holiday Lift Store | Store 7 (+19.4%) |

### Seasonal Patterns

| Category | Period | Average Weekly Sales |
|----------|--------|---------------------|
| Best Month | December | $1,281,864 |
| Worst Month | January | $923,885 |
| Month Difference | December vs January | +38.7% |
| Best Season | Winter | $1,094,937 |
| Worst Season | Spring | $1,023,801 |
| Q4 vs Q1 | Oct-Dec vs Jan-Mar | +12.2% |

### Year-over-Year Trends

| Year | Total Sales | Growth Rate |
|------|-------------|-------------|
| 2010 | $2,288.9 Million | Baseline |
| 2011 | $2,448.2 Million | +7.0% |
| 2012 | $2,000.1 Million | -18.3% |

### Economic Factor Correlations

| Factor | Correlation | Strength | Direction |
|--------|-------------|----------|-----------|
| Unemployment | -0.106 | Weak | Negative |
| CPI | -0.073 | Very Weak | Negative |
| Temperature | -0.064 | Very Weak | Negative |
| Fuel Price | +0.009 | Very Weak | Positive |

## Visualizations

The analysis includes the following visualizations saved in the `charts/` directory:

1. **Sales Trend Over Time** - Line chart showing weekly sales with holiday indicators
2. **Top 10 Stores** - Horizontal bar chart ranking stores by total sales
3. **Holiday vs Non-Holiday Sales** - Pie chart and bar chart comparing sales
4. **Monthly Sales Pattern** - Line chart showing seasonal trends
5. **Correlation Heatmap** - Visual representation of factor correlations
6. **Temperature vs Sales** - Scatter plot analyzing temperature impact

## Recommendations

### Short-Term Actions (Next Quarter)

| Priority | Recommendation | Expected Impact |
|----------|----------------|------------------|
| High | Investigate 2012 sales decline across all stores | Identify root causes |
| High | Analyze underperforming stores (33, 44, 5, 36, 38) | Unlock hidden revenue |
| Medium | Implement holiday best practices from Stores 7, 35, 15 | Increase holiday lift |
| Medium | Optimize inventory for December peak | Reduce stockouts |

### Long-Term Strategies (Next 12 Months)

1. **Address the 2012 Sales Decline**
   - Conduct store-level audits for declining locations
   - Review pricing, promotions, and competitive positioning
   - Analyze customer traffic patterns versus 2011 baseline

2. **Leverage Store Performance Gaps**
   - Study best practices from top-performing stores
   - Create performance improvement plans for bottom 5 stores
   - Consider store format changes for consistent low performers

3. **Maximize Holiday Opportunities**
   - Concentrate marketing spend on the 7% of weeks that drive premium sales
   - Pre-holiday inventory build-up starting September
   - Develop store-specific holiday strategies for low-lift locations

4. **Optimize Seasonal Operations**
   - Ramp up staffing and inventory from September through December
   - Plan post-holiday clearance for January
   - Align marketing campaigns with monthly sales patterns

## Key Conclusions

### What Works
- Holiday promotions deliver +7.8% sales lift
- December peak season drives maximum revenue
- Top stores demonstrate replicable success models

### What Needs Attention
- 18.3% sales decline from 2011 to 2012 requires investigation
- 8.1x performance gap between best and worst stores
- Post-holiday drop significantly impacts Q1 performance

### What Doesn't Matter Much
- Temperature has virtually no impact on sales
- Fuel prices show minimal correlation
- CPI provides weak predictive value

### Final Takeaway
Walmart's sales are driven primarily by seasonal timing and holiday events, not by broad economic factors. The performance gap between stores and the 2012 decline represent the biggest opportunities for intervention.

## Requirements
pandas
numpy
matplotlib
seaborn
fpdf (for PDF report generation)

text

## Installation

```bash
pip install pandas numpy matplotlib seaborn fpdf2
Usage
Place the Walmart_Sales.csv file in the data/ directory

Run the Jupyter notebook walmart_sales_analysis.ipynb

The analysis will generate:

Cleaned data in outputs/walmart_cleaned.csv

Summary metrics in outputs/walmart_analysis_summary.csv

Charts in the charts/ directory

PDF report in the reports/ directory

Output Files
File	Description
walmart_cleaned.csv	Cleaned dataset with engineered features (Year, Month, Season, Sales_Category, etc.)
walmart_analysis_summary.csv	Key metrics and KPIs in tabular format
walmart_analysis_report.pdf	Professional PDF report with all findings and recommendations
Report Generation
To generate the PDF report, run the final cell in the notebook. The report includes:

Executive Summary

Key Performance Metrics

Store Performance Analysis

Holiday Impact Analysis

Seasonal Patterns

Economic Factor Correlations

Year-over-Year Trends

Recommendations

Conclusions

Appendix with Data Summary

Author
GEORGE ONYANGO OCHIENG
georgebabji1220@gmail.com
georgeonyango1220@gmail.com
Date
May 2026
