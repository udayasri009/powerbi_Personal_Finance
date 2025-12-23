# powerbi_Personal_Finance
## Project Objective
The objective of this project is to monitor and analyze income performance against predefined monthly targets using interactive Power BI dashboards. The project focuses on comparing actual income with income goals, identifying performance gaps, and tracking achievement levels across different time periods and categories. By integrating transactional data with income targets, the dashboard provides key KPIs such as Total Income, Target Income, Variance, and Achievement Percentage.

## Dataset used
- <a href ="https://github.com/udayasri009/powerbi_Personal_Finance/blob/main/Dataset.xlsx">Dataset</a>

## Questions

How did you calculate Total Actual Income?

How did you calculate Total Income Target?

How did you calculate Variance?

Why did you use the DIVIDE function instead of normal division?

How did you calculate Achievement Percentage?

How did you handle divide-by-zero errors?

How do slicers affect DAX measures?

## formulas
Total Actual Income =
SUM('Main Data'[Amount])

Total Income Target =
SUM('Income Goal'[Income Target])

Income Variance =
[Total Income Target] - [Total Actual Income]

Achievement % =
DIVIDE([Total Actual Income], [Total Income Target], 0)


Over Target =
IF(
    [Total Actual Income] > [Total Income Target],
    [Total Actual Income] - [Total Income Target],
    0
)

Pending Target =
IF(
    [Total Actual Income] < [Total Income Target],
    [Total Income Target] - [Total Actual Income],
    0
)

## DASHBOARD 
![powerbi_personal_finance](https://github.com/udayasri009/powerbi_Personal_Finance/blob/main/personal_finance.img.png)

## Project Insight
The dashboard highlighted key performance gaps between actual income and targets, identified top-performing categories, and revealed periods of underachievement. These insights help stakeholders monitor progress, optimize targets, and improve overall income performance.

## Final conclusion
The Income Monitoring Dashboard successfully transforms raw financial data into meaningful and actionable insights by clearly comparing actual income against predefined targets. Through interactive KPI cards, trend analysis, and category-level breakdowns, the dashboard enables continuous tracking of income performance and highlights variances that require immediate attention.
