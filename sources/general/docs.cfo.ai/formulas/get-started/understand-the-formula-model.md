# Source: https://docs.cfo.ai/formulas/get-started/understand-the-formula-model

A formula tells cfo.ai how to calculate a Variable. It works much like a spreadsheet formula, but it points to named business concepts such as Revenue instead of cell positions such as `B7`. The Variable names the result, the expression defines the calculation, and the formula’s scope determines which Model values it controls. That business meaning stays the same when you or Ari view the result in a different table. If these concepts are new, start with [What is a Variable?](https://docs.cfo.ai/formulas/core-concepts/variables-and-dimensions/what-is-a-variable). For example, a **Gross Profit** Variable might use this formula:

```
Revenue - `Cost of Goods Sold`
```

Variable names with spaces are wrapped in backticks.

## 

[​](https://docs.cfo.ai/formulas/get-started/understand-the-formula-model#every-formula-has-an-expression-and-a-scope)

Every formula has an expression and a scope

Every saved formula combines two parts:

- **Expression:** what to calculate.
- **Scope:** which Dimensions, segments, or time ranges the calculation applies to.

The expression above calculates Gross Profit. Its scope might apply everywhere, whenever the Model is segmented by Department, or only to Department = Sales.

## 

[​](https://docs.cfo.ai/formulas/get-started/understand-the-formula-model#a-variable-can-have-more-than-one-formula)

A Variable can have more than one formula

A Variable can use different formulas in different parts of a model. You might use:

- One default formula across the model
- A different formula for a particular department
- One formula for Actuals and another for Forecast

cfo.ai chooses the matching formula for each value it calculates. A specific formula can override a broader formula without replacing the default everywhere.

## 

[​](https://docs.cfo.ai/formulas/get-started/understand-the-formula-model#variables-and-dimensions-do-different-jobs)

Variables and Dimensions do different jobs

A **Variable** holds a value. A **Dimension** organizes that value by a business category or time period. When Revenue is shown by Department, Revenue is the Variable, Department is the Dimension, and Sales is a Dimension item. Revenue for Sales is a segment of Revenue.

## 

[​](https://docs.cfo.ai/formulas/get-started/understand-the-formula-model#references-follow-the-current-cell)

References follow the current cell

A plain Variable reference follows the current segment. If a formula is calculating a value for Sales in March, a reference to `Headcount` reads the Sales headcount for the same period when that context applies. You can choose a different segment explicitly:

```
Revenue[Department = "Sales"]
```

Use a suffix `$` when a reference should not inherit the current segment:

```
Revenue$[Department = "Sales"]
```

## 

[​](https://docs.cfo.ai/formulas/get-started/understand-the-formula-model#time-and-scenarios-provide-context)

Time and Scenarios provide context

The same Variable can use different formulas in Actuals and Forecast, and a Scenario can hold its own version of a plan. Name the Scenario and formula range whenever that choice matters to the result.

## 

[​](https://docs.cfo.ai/formulas/get-started/understand-the-formula-model#next-step)

Next step

Use [Write your first formula](https://docs.cfo.ai/formulas/get-started/write-your-first-formula) to create a calculation and verify the values it produces.

Ctrl+I