# Source: https://docs.cfo.ai/formulas/formula-reference/function-reference/math-functions

Math functions transform numeric values.

## 

[​](https://docs.cfo.ai/formulas/formula-reference/function-reference/math-functions#abs)

abs

Returns the absolute value of a number.

```
abs(Actual - Plan)
```

A negative value becomes positive. A positive value stays positive.

## 

[​](https://docs.cfo.ai/formulas/formula-reference/function-reference/math-functions#sqrt)

sqrt

Returns the square root of a number.

```
sqrt(Variance)
```

The input must be zero or positive. Use conditional logic if the input can be negative:

```
if(Variance >= 0, sqrt(Variance), 0)
```

## 

[​](https://docs.cfo.ai/formulas/formula-reference/function-reference/math-functions#ceiling)

ceiling

Rounds a number up to the nearest multiple of a specified significance.

```
ceiling(`Unit Price`, 0.05)
```

This follows Excel `CEILING` behavior.

## 

[​](https://docs.cfo.ai/formulas/formula-reference/function-reference/math-functions#floor)

floor

Rounds a number down to the nearest multiple of a specified significance.

```
floor(`Unit Price`, 0.05)
```

This follows Excel `FLOOR` behavior.

## 

[​](https://docs.cfo.ai/formulas/formula-reference/function-reference/math-functions#round)

round

Rounds a number to the requested number of digits.

```
round(Forecast, 2)
```

This follows Excel `ROUND` behavior.

Ctrl+I