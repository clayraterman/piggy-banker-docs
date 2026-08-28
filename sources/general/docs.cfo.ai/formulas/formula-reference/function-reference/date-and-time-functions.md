# Source: https://docs.cfo.ai/formulas/formula-reference/function-reference/date-and-time-functions

These functions build dates, shift them, compare them, or return information about a period.

## 

[​](https://docs.cfo.ai/formulas/formula-reference/function-reference/date-and-time-functions#dateadd)

dateadd

Shifts a date by a signed amount.

```
dateadd(Date.Month, -1, "month")
```

Supported units are `"day"`, `"week"`, `"month"`, `"quarter"`, `"half"`, and `"year"`. The amount is a signed whole number, and the unit must be quoted.

## 

[​](https://docs.cfo.ai/formulas/formula-reference/function-reference/date-and-time-functions#datedif)

datedif

Returns the difference between a start date and end date using an Excel-style unit code.

```
datedif(`Start Date`, Date.Month, "M")
```

Supported codes include `Y`, `M`, `D`, `MD`, `YM`, and `YD`. The start date must not be after the end date.

## 

[​](https://docs.cfo.ai/formulas/formula-reference/function-reference/date-and-time-functions#daysin)

daysin

Returns the number of days in the aligned period containing a date.

```
daysin(Date.Month, "month")
```

Supported units are day, week, month, quarter, half, and year.

## 

[​](https://docs.cfo.ai/formulas/formula-reference/function-reference/date-and-time-functions#date)

date

Builds a date from year, month, and day numbers.

```
date(2026, 12, 31)
date(year(Date.Month), 12, 31)
```

Month and day values can roll into adjacent periods, following Excel `DATE` behavior for normal supported dates.

## 

[​](https://docs.cfo.ai/formulas/formula-reference/function-reference/date-and-time-functions#edate)

edate

Shifts a date by whole months and clamps the day to the target month when needed.

```
edate(Date.Month, 3)
```

## 

[​](https://docs.cfo.ai/formulas/formula-reference/function-reference/date-and-time-functions#eomonth)

eomonth

Returns the last day of a month a signed number of months from a date.

```
eomonth(Date.Month, 0)
```

Use `0` for the current month, `1` for the next month, and `-1` for the previous month.

## 

[​](https://docs.cfo.ai/formulas/formula-reference/function-reference/date-and-time-functions#related)

Related

- [Work with dates](https://docs.cfo.ai/formulas/formula-guides/work-with-dates)
- [Date-part functions](https://docs.cfo.ai/formulas/formula-reference/function-reference/date-part-functions)

Ctrl+I