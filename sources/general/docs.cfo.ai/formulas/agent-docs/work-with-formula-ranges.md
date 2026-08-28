# Source: https://docs.cfo.ai/formulas/agent-docs/work-with-formula-ranges

Formula ranges separate parts of the timeline that use different calculations. Actuals and Forecast are defined relative to the workspace’s Last close date.

## 

[​](https://docs.cfo.ai/formulas/agent-docs/work-with-formula-ranges#start-from-the-saved-table)

Start from the saved table

When the requested formula belongs to a visible row, column, or cell, inspect the saved Table Block and use `edit_table_blocks` to target the actual result. The server derives the applicable formula range from the selected visible target. You do not need to invent or fetch a formula-range ID for a visible edit.

## 

[​](https://docs.cfo.ai/formulas/agent-docs/work-with-formula-ranges#date-scope-is-required)

Date scope is required

A rule for Actuals or Forecast needs Date in its condition at the Model’s base grain. For a monthly Model:

```
[Date.Month in any]
```

```
[Department = "Sales", Date.Month in any]
```

For a table-independent formula, use `edit_variables` with `action: "set_values"`, the Date-aware condition, and `period: "actuals"` or `period: "forecast"`.

## 

[​](https://docs.cfo.ai/formulas/agent-docs/work-with-formula-ranges#read-last-close-when-it-matters)

Read Last close when it matters

Use `inspect_dimensions` to inspect the Date Dimension and its time settings when you need to confirm Last close. The boundary affects which dates count as Actuals and which belong to Forecast. If Last close is missing, explain the missing workspace setting before trying to build a range-dependent result.

## 

[​](https://docs.cfo.ai/formulas/agent-docs/work-with-formula-ranges#preserve-the-model%E2%80%99s-time-grain)

Preserve the Model’s time grain

Use the workspace’s actual Date grain rather than assuming every Model is monthly. Date-aware conditions, selected table periods, and the user’s requested range must agree.

## 

[​](https://docs.cfo.ai/formulas/agent-docs/work-with-formula-ranges#verify-both-sides-of-the-boundary)

Verify both sides of the boundary

After the change, inspect one period in Actuals and one in Forecast. Verify that the intended rule applies only where it should and that the chosen Scenario contains the saved change.

Ctrl+I