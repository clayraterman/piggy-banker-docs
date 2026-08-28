# Source: https://docs.cfo.ai/dashboards/build-and-format-tables

A Table Block has two concerns that you or Ari can change independently: **what it calculates** and **how it is presented**. You can restyle a table without changing its numbers, or restructure its numbers without losing the surrounding presentation.

## 

[​](https://docs.cfo.ai/dashboards/build-and-format-tables#what-a-table-block-calculates)

What a Table Block calculates

Ask Ari to set:

- **Variables** — which Variables appear, in what order, each becoming a row.
- **Dimensions and time** — how to segment those Variables by one or more business categories, or by a Date grain such as month or quarter.
- **Window** — the date range and grain a new table shows. Reconfiguring an existing table’s Variables leaves its window alone; change the window through presentation instead.
- **Transpose** — flip rows and columns, useful for a database-style list of items with attributes across the top instead of a wide row of dates.

Ask Ari to check a table’s declaration for problems, like an axis pointing at a Variable that no longer exists, before assuming a blank result means something is wrong with the numbers themselves.

## 

[​](https://docs.cfo.ai/dashboards/build-and-format-tables#how-a-table-block-is-presented)

How a Table Block is presented

Once a table calculates the right thing, ask Ari to adjust its presentation without touching the calculation:

- **Rename** the block’s title.
- **Columns** — widths and whether the formula column is visible.
- **Visibility** — hide or show specific rows or columns without deleting them.
- **Window** — change the shown date range or grain on an existing table.
- **Comparison** — show another Scenario, or an earlier period, alongside the baseline. See [Create and compare Scenarios](https://docs.cfo.ai/scenarios/create-and-compare-scenarios).
- **Sort** — order an axis ascending, descending, or in a manual order you specify.
- **Formatting** — fill color, bold, italic, underline, strikethrough, and row indent, applied to a whole row, a whole column, or a specific cell.
- **Transpose** — layout only, the same table read the other way.

## 

[​](https://docs.cfo.ai/dashboards/build-and-format-tables#copy-a-table-block)

Copy a Table Block

Ask Ari to copy an existing table onto a new or different Page. The original is left alone, and the copy starts from the same Variables and Dimensions so you can reshape it independently.

## 

[​](https://docs.cfo.ai/dashboards/build-and-format-tables#custom-visualizations)

Custom visualizations

When a grid isn’t the right shape for what you want to show, like a trend line or a KPI scorecard, ask Ari to build a code block instead. A code block pulls live data out of your Model the same way a Table Block does, but renders it as a chart, scorecard, or interactive control.

## 

[​](https://docs.cfo.ai/dashboards/build-and-format-tables#inspect-formulas-and-segments)

Inspect formulas and segments

Use **Segment by** to expose a Variable’s values by another Dimension. Use **Drill in** when you want to see the formula inputs behind a calculated result. These actions answer different questions: **Segment by** asks how a value is distributed, while **Drill in** asks which inputs produced it.

## 

[​](https://docs.cfo.ai/dashboards/build-and-format-tables#related)

Related

- [Pages and blocks](https://docs.cfo.ai/dashboards/pages-and-blocks)
- [Segments and segmentations](https://docs.cfo.ai/formulas/core-concepts/segments-and-segmentations)

Ctrl+I