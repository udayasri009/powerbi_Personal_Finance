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
![powerbi_personal_finance](POWERBI_DASHBOARD.IMG.png)

## Project Insight

