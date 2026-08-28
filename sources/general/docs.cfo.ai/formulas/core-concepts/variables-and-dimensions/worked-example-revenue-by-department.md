# Source: https://docs.cfo.ai/formulas/core-concepts/variables-and-dimensions/worked-example-revenue-by-department

This example shows how Variables, Dimensions, segments, and formulas work together.

## 

[​](https://docs.cfo.ai/formulas/core-concepts/variables-and-dimensions/worked-example-revenue-by-department#the-business-question)

The business question

> How much Revenue did each Department produce by month in the Plan scenario?

## 

[​](https://docs.cfo.ai/formulas/core-concepts/variables-and-dimensions/worked-example-revenue-by-department#the-variables-and-dimensions)

The Variables and Dimensions

- **Revenue** is a Variable. It is the value being measured.
- **Department** is a Dimension. It organizes Revenue by team.
- **Date** is a Dimension. It organizes Revenue by month.

Plan is the Scenario used for the calculation.

## 

[​](https://docs.cfo.ai/formulas/core-concepts/variables-and-dimensions/worked-example-revenue-by-department#the-cell-address)

The cell address

One result might be:

> Revenue = 250,000 for Department = Sales in January 2026 in Plan

Revenue is the Variable. Sales is a Department item, January 2026 is the Date period, and Plan provides the Scenario context. Together, the Variable, Dimension item, and period identify the cell address.

## 

[​](https://docs.cfo.ai/formulas/core-concepts/variables-and-dimensions/worked-example-revenue-by-department#the-table)

The table

A familiar table might place:

- Revenue on rows
- Month on columns
- Department exposed with **Segment by**.

The layout does not create new business concepts. It arranges the same Variables and Dimensions so people can answer a question.

## 

[​](https://docs.cfo.ai/formulas/core-concepts/variables-and-dimensions/worked-example-revenue-by-department#the-formula)

The formula

Suppose planned Revenue is calculated as:

```
`Units Sold` * Price
```

Revenue is the target Variable. Units Sold and Price are the referenced Variables. The backticks around `Units Sold` preserve the space in its name. When the table is broken down by Department, plain references follow the current Department segment. The Sales Revenue cell uses Sales Units Sold and Sales Price when those Variables share the same context.

## 

[​](https://docs.cfo.ai/formulas/core-concepts/variables-and-dimensions/worked-example-revenue-by-department#a-segment-specific-exception)

A segment-specific exception

If Sales uses a different pricing rule, Revenue can have a more specific formula for Department = Sales. The broader Revenue formula continues to apply to other departments. Variables hold the values, Dimensions organize them, segments describe meaningful slices, and a cell address identifies one exact result.

Ctrl+I