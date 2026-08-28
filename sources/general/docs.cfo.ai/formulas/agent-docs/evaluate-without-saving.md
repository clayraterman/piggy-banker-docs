# Source: https://docs.cfo.ai/formulas/agent-docs/evaluate-without-saving

A read-only analysis starts with saved Model content. Inspect existing Table Blocks, Variables, Scenarios, and source information without creating a new calculation.

## 

[​](https://docs.cfo.ai/formulas/agent-docs/evaluate-without-saving#read-a-saved-table-block)

Read a saved Table Block

Use `inspect_table_blocks` with the table that contains the values:

```
{
  "scenario": "Main",
  "tables": ["Revenue by Customer"],
  "formula_origins": "all"
}
```

Copy row and column references from the response when narrowing a follow-up to a visible row, cell, or subtree.

## 

[​](https://docs.cfo.ai/formulas/agent-docs/evaluate-without-saving#compare-or-rank-existing-values)

Compare or rank existing values

Use the saved table’s existing Scenario or time comparison when it already answers the question. For a top-items question, pass the supported `rank` argument to `inspect_table_blocks` with exactly one saved Table Block.

```
{
  "scenario": "Main",
  "tables": ["Revenue by Customer"],
  "rank": {
    "dimension": "Customer",
    "n": 5,
    "by": "value",
    "direction": "desc"
  }
}
```

Historical reads use `as_of_point` against the same saved table and the same target. That keeps the before-and-after comparison tied to one stable artifact.

## 

[​](https://docs.cfo.ai/formulas/agent-docs/evaluate-without-saving#validate-without-applying-a-change)

Validate without applying a change

When the user asks whether a proposed formula would be accepted, use `dry_run: true` on a supported `edit_table_blocks` or `edit_variables` formula write. The result validates the proposed write without saving it. A dry run checks the write. It does not create a new calculated series to inspect.

## 

[​](https://docs.cfo.ai/formulas/agent-docs/evaluate-without-saving#create-a-result-only-when-authorized)

Create a result only when authorized

A new ratio, signal, or comparison that does not already exist needs a saved visible Model artifact. If the user authorizes that work, use `edit_table_blocks` to add a row and its initial formula, then inspect the saved result. If the user asked for no Model changes, explain the existing information you can answer from and identify the saved change a new calculation would require.

Ctrl+I