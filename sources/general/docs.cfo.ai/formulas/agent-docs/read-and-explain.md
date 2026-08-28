# Source: https://docs.cfo.ai/formulas/agent-docs/read-and-explain

Use `inspect_variables` with `saved_formulas` when a user asks how a Variable is calculated or why its behavior changes by segment or period.

## 

[​](https://docs.cfo.ai/formulas/agent-docs/read-and-explain#read-the-saved-rules)

Read the saved rules

For example:

```
{
  "scenario": "Main",
  "saved_formulas": {
    "variables": ["Gross Margin"]
  }
}
```

Add `conditions` only when the question requires one exact saved scope. Omit the filter when the user wants the complete set of rules.

## 

[​](https://docs.cfo.ai/formulas/agent-docs/read-and-explain#connect-rules-to-visible-values)

Connect rules to visible values

Use `inspect_table_blocks` for the table that actually shows the result. Request `formula_origins: "all"` when the explanation depends on which rule filled a row or cell.

```
{
  "scenario": "Main",
  "tables": ["Operating Plan"],
  "formula_origins": "all"
}
```

Use the same requested Scenario for both the saved-formula read and the table inspection. The saved rule explains the intended calculation. The visible table confirms which rule actually applies to the selected period, segment, and Scenario.

## 

[​](https://docs.cfo.ai/formulas/agent-docs/read-and-explain#historical-reads)

Historical reads

Use `as_of_point` when the user asks for the Model as it existed at a previous saved change. Omit it for the current state.

## 

[​](https://docs.cfo.ai/formulas/agent-docs/read-and-explain#explain-the-business-meaning)

Explain the business meaning

Lead with what the formula does, then explain the inputs, the Scenario, the relevant Dimensions, and whether Actuals or Forecast changes the result. Include assumptions only when they matter to the user’s question.

Ctrl+I