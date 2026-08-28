# Source: https://docs.cfo.ai/formulas/formula-reference/function-reference/conditional-functions

## 

[​](https://docs.cfo.ai/formulas/formula-reference/function-reference/conditional-functions#if)

if

Returns one of two values based on a condition.

```
if(condition, value_when_true, value_when_false)
```

Example:

```
if(Revenue > 0, `Gross Profit` / Revenue, 0)
```

The three arguments are:

1. A condition
2. The result when the condition is true
3. The result when the condition is false

The two result expressions should represent compatible types. You can nest `if` calls:

```
if(Revenue > 100, "high", if(Revenue > 50, "medium", "low"))
```

For several categories or exceptions, a dimension-based formula may be easier to maintain than a deeply nested expression.

## 

[​](https://docs.cfo.ai/formulas/formula-reference/function-reference/conditional-functions#iferror)

iferror

Returns the first expression when it succeeds, or the fallback when that expression produces a calculation error.

```
iferror(value, value_if_error)
```

For example:

```
iferror(`Gross Profit` / Revenue, 0)
```

If Revenue is zero, the division creates a cell-level error and `iferror` returns `0` instead. You can also use it with date calculations:

```
iferror(datedif(`Start Date`, Date.Month, "M"), 0)
```

Ctrl+I