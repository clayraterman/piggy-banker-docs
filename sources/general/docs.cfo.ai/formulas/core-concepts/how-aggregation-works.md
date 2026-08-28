# Source: https://docs.cfo.ai/formulas/core-concepts/how-aggregation-works

Aggregation combines several values into one result. The correct aggregation depends on the business question, not only on how a Table Block is arranged.

## 

[​](https://docs.cfo.ai/formulas/core-concepts/how-aggregation-works#1-variable-aggregation)

1\. Variable aggregation

A Variable has a default method for combining source records into a Model value. Numeric flows such as revenue or expenses commonly use `sum`. Balances, ratios, headcount, and other point-in-time results can require a different time rollup. For example, a quarter-end cash balance should show the closing balance rather than adding three monthly balances together.

## 

[​](https://docs.cfo.ai/formulas/core-concepts/how-aggregation-works#2-multi-value-references)

2\. Multi-value references

A formula reference can deliberately select several values. For example:

```
Revenue[Department in any]
```

This selects Revenue across all Department items. A multi-value Variable lookup uses a sum when another aggregation is not stated. It is clearer to write the intended aggregation when the choice matters:

```
average(Revenue[Department in any])
```

## 

[​](https://docs.cfo.ai/formulas/core-concepts/how-aggregation-works#3-aggregation-functions)

3\. Aggregation functions

Aggregation functions let you choose how several values become one result. Available functions:

- `sum` and `product`.
- `average`.
- `min` and `max`.
- `count`.
- `first` and `last`.
- `median`.
- `stdev` and `var`.

Most numeric aggregation functions accept up to 10 expressions. `first`, `last`, and `median` each accept one expression.

## 

[​](https://docs.cfo.ai/formulas/core-concepts/how-aggregation-works#example)

Example

If Department Revenue is Sales 50, Marketing 30, and Engineering 20:

- `sum(Revenue[Department in any])` returns 100.
- `average(Revenue[Department in any])` returns about 33.33.
- `max(Revenue[Department in any])` returns 50.
- `median(Revenue[Department in any])` returns 30.
- `count(Revenue[Department in any])` returns 3 when all three values are present.

## 

[​](https://docs.cfo.ai/formulas/core-concepts/how-aggregation-works#write-the-business-meaning)

Write the business meaning

Use the aggregation that matches the question. Totals usually use `sum`. Rates and ratios often need to be recalculated from their underlying totals instead of averaged after the fact.

## 

[​](https://docs.cfo.ai/formulas/core-concepts/how-aggregation-works#related)

Related

- [Aggregation function reference](https://docs.cfo.ai/formulas/formula-reference/function-reference/aggregation-functions)
- [Common formula patterns](https://docs.cfo.ai/formulas/formula-guides/common-formula-patterns)

Ctrl+I