# Source: https://docs.cfo.ai/formulas/formula-reference/function-reference/aggregation-functions

Aggregation functions combine several selected values into one result.

## 

[​](https://docs.cfo.ai/formulas/formula-reference/function-reference/aggregation-functions#sum-and-product)

sum and product

`sum` adds selected numeric values. `product` multiplies them.

```
sum(Revenue[Department in any])
product(`Growth Factor`[Date.Month in any])
```

Both functions accept one to 10 expressions.

## 

[​](https://docs.cfo.ai/formulas/formula-reference/function-reference/aggregation-functions#average)

average

Returns the arithmetic mean, or null when no values exist.

```
average(Revenue[Department in any])
```

`average` is the preferred spelling. Existing formulas using `avg` remain supported.

## 

[​](https://docs.cfo.ai/formulas/formula-reference/function-reference/aggregation-functions#min-and-max)

min and max

Return the smallest or largest value, or null when no values exist.

```
min(Revenue[Department in any])
max(Revenue[Department in any])
```

## 

[​](https://docs.cfo.ai/formulas/formula-reference/function-reference/aggregation-functions#count)

count

Counts non-empty values of any type. It behaves like Excel `COUNTA`, not Excel `COUNT`.

```
count(Orders[Department in any])
```

## 

[​](https://docs.cfo.ai/formulas/formula-reference/function-reference/aggregation-functions#first-and-last)

first and last

Return the first or last value in the selected series order, or null when the series is empty.

```
first(Revenue[Date.Month in any])
last(Revenue[Date.Month in any])
```

Both functions accept one expression.

## 

[​](https://docs.cfo.ai/formulas/formula-reference/function-reference/aggregation-functions#median)

median

Returns the middle numeric value when the selection has an odd number of values. When the count is even, it returns the average of the two middle values. It returns null when no values exist.

```
median(`Annual Salary`[Employee in any])
```

`median` accepts one expression.

## 

[​](https://docs.cfo.ai/formulas/formula-reference/function-reference/aggregation-functions#stdev-and-var)

stdev and var

`stdev` returns sample standard deviation. `var` returns sample variance. Both use the sample calculation with one degree of freedom and return null when fewer than two values are present.

```
stdev(Revenue[Region in any])
var(Revenue[Region in any])
```

Both functions accept one to 10 expressions. Existing formulas using `stddev` or `variance` remain supported, but `stdev` and `var` are preferred.

## 

[​](https://docs.cfo.ai/formulas/formula-reference/function-reference/aggregation-functions#combine-multiple-expressions)

Combine multiple expressions

`sum`, `product`, `average`, `count`, `min`, `max`, `stdev`, and `var` can combine up to 10 expressions:

```
sum(Revenue[Region in any], `Other Income`[Region in any])
```

`average` pools the underlying values rather than averaging the average of each expression.

Ctrl+I