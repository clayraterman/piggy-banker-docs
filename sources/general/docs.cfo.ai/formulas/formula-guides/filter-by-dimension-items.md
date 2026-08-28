# Source: https://docs.cfo.ai/formulas/formula-guides/filter-by-dimension-items

A Variable lookup can select one Dimension item, a chosen set of items, or every item in a Dimension.

## 

[​](https://docs.cfo.ai/formulas/formula-guides/filter-by-dimension-items#select-one-item)

Select one item

```
Revenue[Department = "Sales"]
```

This changes Department to Sales while other dimensions continue to follow the current segment.

## 

[​](https://docs.cfo.ai/formulas/formula-guides/filter-by-dimension-items#select-several-items)

Select several items

Use a set:

```
Revenue[Department in {"Engineering", "Product", "Design"}]
```

A multi-value lookup is summed when no aggregation function is written. Add the intended function when another behavior is clearer:

```
average(Revenue[Department in {"Engineering", "Product", "Design"}])
```

## 

[​](https://docs.cfo.ai/formulas/formula-guides/filter-by-dimension-items#exclude-selected-items)

Exclude selected items

```
Revenue[Department not in {"Engineering"}]
```

## 

[​](https://docs.cfo.ai/formulas/formula-guides/filter-by-dimension-items#select-every-item)

Select every item

```
Revenue[Department in any]
```

This is useful for totals, averages, and percent-of-total calculations.

## 

[​](https://docs.cfo.ai/formulas/formula-guides/filter-by-dimension-items#filter-with-an-expression)

Filter with an expression

Use `where` when the selected segment must meet an additional condition:

```
sum(Revenue[Department in any] where Revenue > 10000)
```

In this example, the condition keeps only Department segments whose Revenue exceeds 10,000. Use `this` when you need to refer to the current formula context from within a filter:

```
sum(Revenue[Department in any] where Revenue > this.Revenue)
```

## 

[​](https://docs.cfo.ai/formulas/formula-guides/filter-by-dimension-items#combine-dimensions)

Combine dimensions

```
Revenue[Region = "West", Department = "Sales"]
```

Keep filters as narrow as the business rule requires. If the current segment already matches the intended result, use a plain Variable reference.

Ctrl+I