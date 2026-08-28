# Source: https://docs.cfo.ai/formulas/agent-docs/create-and-update

A saved formula belongs to its Variable. When the user selects a visible row, column, or cell, the saved Table Block provides the target that resolves the correct Variable and scope.

## 

[​](https://docs.cfo.ai/formulas/agent-docs/create-and-update#write-through-the-saved-table)

Write through the saved table

First use `inspect_table_blocks` to obtain the visible row and column references. Then send the related formula edits together using `edit_table_blocks`. Pass the same requested Scenario to the inspection and the write so they resolve the same saved table.

```
{
  "scenario": "Main",
  "table": "Operating Plan",
  "edits": [
    {
      "target": {
        "kind": "row",
        "row": "<row reference returned by the table inspection>"
      },
      "action": "set_formula",
      "formula": "Revenue - `Cost of Goods Sold`"
    }
  ]
}
```

The server derives the Variable, cell address, formula range, and write permissions from the visible target. Copy references from the inspection result instead of inventing IDs, positions, or range identifiers.

## 

[​](https://docs.cfo.ai/formulas/agent-docs/create-and-update#create-a-visible-derived-row)

Create a visible derived row

A new Variable can be defined and placed on a saved Table Block in the same change:

```
{
  "scenario": "Main",
  "table": "Operating Plan",
  "edits": [
    {
      "target": { "kind": "table" },
      "action": "insert",
      "kind": "variable",
      "name": "Gross Margin",
      "formula": "iferror(`Gross Profit` / Revenue, 0)"
    }
  ]
}
```

The saved row makes the calculation visible, inspectable, and available for follow-up.

## 

[​](https://docs.cfo.ai/formulas/agent-docs/create-and-update#use-a-table-independent-write-only-when-appropriate)

Use a table-independent write only when appropriate

Use `edit_variables` with `action: "set_values"` when the requested rule has no saved table target. Send related items together and provide the intended Scenario, formula scope, and time range. `dry_run: true` validates supported formula writes without applying them. `mode: "atomic"` makes the selected batch succeed together or fail together; the default partial mode can apply valid items and report invalid ones.

## 

[​](https://docs.cfo.ai/formulas/agent-docs/create-and-update#verify-the-saved-result)

Verify the saved result

Read the affected Table Block after a material change. Check the intended Scenario, representative dates and segments, formula origins, and the actual numeric result. When a batch reports rejected items, distinguish saved changes from unsuccessful ones and retry only the work that still needs correction.

Ctrl+I