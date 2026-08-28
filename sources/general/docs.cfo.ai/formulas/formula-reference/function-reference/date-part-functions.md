# Source: https://docs.cfo.ai/formulas/formula-reference/function-reference/date-part-functions

Date-part functions return a numeric part of a date.

## 

[​](https://docs.cfo.ai/formulas/formula-reference/function-reference/date-part-functions#year)

year

Returns the four-digit year.

```
year(Date.Month)
```

## 

[​](https://docs.cfo.ai/formulas/formula-reference/function-reference/date-part-functions#month)

month

Returns the month as a number from 1 to 12.

```
month(Date.Month)
```

## 

[​](https://docs.cfo.ai/formulas/formula-reference/function-reference/date-part-functions#day)

day

Returns the day of the month from 1 to 31.

```
day(Date.Day)
```

## 

[​](https://docs.cfo.ai/formulas/formula-reference/function-reference/date-part-functions#quarter)

quarter

Returns the calendar quarter from 1 to 4.

```
quarter(Date.Month)
```

## 

[​](https://docs.cfo.ai/formulas/formula-reference/function-reference/date-part-functions#half)

half

Returns 1 for January through June and 2 for July through December.

```
half(Date.Month)
```

## 

[​](https://docs.cfo.ai/formulas/formula-reference/function-reference/date-part-functions#weekday)

weekday

Returns the day of the week as a number.

```
weekday(Date.Day)
weekday(Date.Day, 2)
```

Without a return type, Sunday is 1 and Saturday is 7. Optional Excel-compatible return types control the starting day and numbering.

## 

[​](https://docs.cfo.ai/formulas/formula-reference/function-reference/date-part-functions#weeknum)

weeknum

Returns the week number within the year.

```
weeknum(Date.Week)
weeknum(Date.Week, 21)
```

The optional return type follows Excel. Return type 21 uses ISO weeks.

## 

[​](https://docs.cfo.ai/formulas/formula-reference/function-reference/date-part-functions#isoweeknum)

isoweeknum

Returns the ISO 8601 week number.

```
isoweeknum(Date.Week)
```

This is equivalent to `weeknum(Date.Week, 21)`.

## 

[​](https://docs.cfo.ai/formulas/formula-reference/function-reference/date-part-functions#related)

Related

- [Date and time functions](https://docs.cfo.ai/formulas/formula-reference/function-reference/date-and-time-functions)
- [Date-truncation functions](https://docs.cfo.ai/formulas/formula-reference/function-reference/date-truncation-functions)

Ctrl+I