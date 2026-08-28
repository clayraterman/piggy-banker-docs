# Source: https://docs.cfo.ai/formulas/formula-guides/use-conditional-logic

Conditional logic chooses a result based on a test.

## 

[​](https://docs.cfo.ai/formulas/formula-guides/use-conditional-logic#use-if)

Use if

```
if(Revenue > 0, `Gross Profit` / Revenue, 0)
```

The first argument is the test. The second is the result when the test is true. The third is the result when it is false.

## 

[​](https://docs.cfo.ai/formulas/formula-guides/use-conditional-logic#comparisons)

Comparisons

Use:

- `=` for equal
- `<>` for not equal
- `>` and `<`
- `>=` and `<=`

Example:

```
if(Plan = "Enterprise", Revenue * 0.9, Revenue)
```

## 

[​](https://docs.cfo.ai/formulas/formula-guides/use-conditional-logic#combine-tests)

Combine tests

Use `and`, `or`, and `not`:

```
if(Revenue > 0 and `Cost of Goods Sold` > 0, `Gross Profit` / Revenue, 0)
```

## 

[​](https://docs.cfo.ai/formulas/formula-guides/use-conditional-logic#nested-conditions)

Nested conditions

```
if(Revenue > 100, "high", if(Revenue > 50, "medium", "low"))
```

Nested conditions are useful for a small number of clear outcomes. If the formula becomes difficult to read, consider separating the logic into Variables or using dimension-based formulas.

## 

[​](https://docs.cfo.ai/formulas/formula-guides/use-conditional-logic#handle-calculation-errors)

Handle calculation errors

Use a condition when the fallback is part of the business rule:

```
if(Revenue <> 0, `Gross Profit` / Revenue, 0)
```

Use `iferror` when an expression can produce an error and you want a defined fallback:

```
iferror(`Gross Profit` / Revenue, 0)
```

Division by zero produces a cell-level error. `iferror` can catch that error instead of letting it propagate to dependent calculations.

Ctrl+I