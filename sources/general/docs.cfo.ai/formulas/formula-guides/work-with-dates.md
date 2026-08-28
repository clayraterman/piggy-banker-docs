# Source: https://docs.cfo.ai/formulas/formula-guides/work-with-dates

Date references let formulas move through time, group dates, and calculate period boundaries.

## 

[​](https://docs.cfo.ai/formulas/formula-guides/work-with-dates#use-the-table%E2%80%99s-granularity)

Use the table’s granularity

Write Date with the grain used by the formula:

```
Date.Month
Date.Quarter
Date.Year
```

Supported grains are Day, Week, Month, Quarter, Half, and Year.

## 

[​](https://docs.cfo.ai/formulas/formula-guides/work-with-dates#reference-a-nearby-period)

Reference a nearby period

The compact lookup uses the formula’s current Date grain:

```
Revenue[-1]
```

At monthly grain, this reads Revenue from the previous month. A positive value moves forward. For an explicit date shift, use `dateadd`:

```
dateadd(Date.Month, -1, "month")
```

Supported units are day, week, month, quarter, half, and year.

## 

[​](https://docs.cfo.ai/formulas/formula-guides/work-with-dates#select-a-fixed-period)

Select a fixed period

```
Revenue[Date.Month = "2026-01"]
Revenue[Date.Quarter = "2026-Q1"]
Revenue[Date.Year = "2026"]
```

## 

[​](https://docs.cfo.ai/formulas/formula-guides/work-with-dates#select-a-time-window)

Select a time window

Use an inclusive range when a calculation spans several periods:

```
sum(Revenue[Date.Month in "2026-01":"2026-12"])
```

Relative endpoints move with the current period:

```
sum(Revenue[Date.Month in [-12]:[-1]])
```

## 

[​](https://docs.cfo.ai/formulas/formula-guides/work-with-dates#find-a-period-boundary)

Find a period boundary

```
startofmonth(Date.Month)
startofquarter(Date.Month)
```

`startofday`, `startofweek`, `startofhalf`, and `startofyear` are also available. See [Date-truncation functions](https://docs.cfo.ai/formulas/formula-reference/function-reference/date-truncation-functions).

## 

[​](https://docs.cfo.ai/formulas/formula-guides/work-with-dates#read-part-of-a-date)

Read part of a date

```
year(Date.Month)
month(Date.Month)
quarter(Date.Month)
half(Date.Month)
```

Week functions include `weekday`, `weeknum`, and `isoweeknum`. See [Date-part functions](https://docs.cfo.ai/formulas/formula-reference/function-reference/date-part-functions).

## 

[​](https://docs.cfo.ai/formulas/formula-guides/work-with-dates#calculate-a-period-end-or-date-difference)

Calculate a period end or date difference

```
eomonth(Date.Month, 0)
datedif(`Start Date`, Date.Month, "M")
```

## 

[​](https://docs.cfo.ai/formulas/formula-guides/work-with-dates#build-a-date)

Build a date

```
date(year(Date.Month), 12, 31)
```

## 

[​](https://docs.cfo.ai/formulas/formula-guides/work-with-dates#formula-ranges)

Formula ranges

Actuals and Forecast also depend on Date. A formula assigned to a formula range must include the Model’s Date grain in its scope.

## 

[​](https://docs.cfo.ai/formulas/formula-guides/work-with-dates#related)

Related

- [Date and time functions](https://docs.cfo.ai/formulas/formula-reference/function-reference/date-and-time-functions)
- [Actuals, Forecast, and formula ranges](https://docs.cfo.ai/formulas/core-concepts/actuals-forecast-and-formula-ranges)

Ctrl+I