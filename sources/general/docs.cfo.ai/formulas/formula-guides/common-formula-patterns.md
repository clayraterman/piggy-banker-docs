# Source: https://docs.cfo.ai/formulas/formula-guides/common-formula-patterns

These patterns use supported formula syntax. Replace the example Variable and dimension names with names from your model.

## 

[​](https://docs.cfo.ai/formulas/formula-guides/common-formula-patterns#gross-profit)

Gross profit

```
Revenue - `Cost of Goods Sold`
```

## 

[​](https://docs.cfo.ai/formulas/formula-guides/common-formula-patterns#gross-margin)

Gross margin

```
if(Revenue <> 0, (Revenue - `Cost of Goods Sold`) / Revenue, 0)
```

## 

[​](https://docs.cfo.ai/formulas/formula-guides/common-formula-patterns#variance)

Variance

```
Actual - Plan
```

## 

[​](https://docs.cfo.ai/formulas/formula-guides/common-formula-patterns#variance-percentage)

Variance percentage

```
if(Plan <> 0, (Actual - Plan) / Plan, 0)
```

## 

[​](https://docs.cfo.ai/formulas/formula-guides/common-formula-patterns#previous-period-change)

Previous-period change

```
Revenue - Revenue[-1]
```

At monthly grain, this compares the current month with the previous month.

## 

[​](https://docs.cfo.ai/formulas/formula-guides/common-formula-patterns#total-across-a-dimension)

Total across a dimension

```
sum(Revenue[Department in any])
```

## 

[​](https://docs.cfo.ai/formulas/formula-guides/common-formula-patterns#share-of-total)

Share of total

```
iferror(Revenue / sum(Revenue[Department in any]), 0)
```

Because the plain `Revenue` follows the current segment, this produces each department’s share when calculated by Department.

## 

[​](https://docs.cfo.ai/formulas/formula-guides/common-formula-patterns#average-across-selected-segments)

Average across selected segments

```
average(Revenue[Region in {"East", "West"}])
```

## 

[​](https://docs.cfo.ai/formulas/formula-guides/common-formula-patterns#trailing-12-month-revenue)

Trailing 12-month revenue

```
sum(Revenue[Date.Month in [-11]:[0]])
```

The range includes the current month and the preceding 11 months.

## 

[​](https://docs.cfo.ai/formulas/formula-guides/common-formula-patterns#forecast-payroll)

Forecast payroll

```
Headcount * `Average Salary`
```

Assign the formula to Forecast when Actuals should continue to reflect imported data.

## 

[​](https://docs.cfo.ai/formulas/formula-guides/common-formula-patterns#conditional-assumption)

Conditional assumption

```
if(Revenue > 100000, Revenue * 0.05, Revenue * 0.03)
```

## 

[​](https://docs.cfo.ai/formulas/formula-guides/common-formula-patterns#calendar-year-end)

Calendar-year end

```
date(year(Date.Month), 12, 31)
```

The same result can also be expressed as:

```
eomonth(date(year(Date.Month), 12, 1), 0)
```

Before saving a pattern, confirm its target Variable, scope, Date grain, formula range, and Scenario.

Ctrl+I