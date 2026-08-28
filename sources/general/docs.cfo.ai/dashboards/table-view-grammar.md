# Source: https://docs.cfo.ai/dashboards/table-view-grammar

When you ask Ari to build or reshape a Table Block (see [Build and format a Table Block](https://docs.cfo.ai/dashboards/build-and-format-tables)), the shape of its columns is described in a compact grammar called a **breakdown**. You don’t need to write this yourself — Ari does — but knowing the shapes helps you describe what you want precisely.

## 

[​](https://docs.cfo.ai/dashboards/table-view-grammar#the-basic-forms)

The basic forms

- **One Dimension**: `[Department]` splits a row’s values across every Department.
- **A name with spaces**: ``[`Spend Type`]`` — backticks quote a Dimension name that is not a single word.
- **Nested segmentation**: `[Department, Level]` splits by Department, then splits each Department further by Level.
- **Side-by-side split**: `[Department, {Level, Owner}]` splits by Department, then forks into two parallel breakdowns — one by Level, one by Owner — under each Department.
- **A branch condition**: `[Department, {Level[Department = "Engineering"], Owner}]` routes the Level breakdown under Engineering specifically, while Owner applies more broadly.
- **Filtering to specific items**: `[Region in {East, West}]` keeps only the named items instead of showing every item in the Dimension.
- **A date grain**: `[Date.Month]` buckets a date Dimension at a chosen grain — Day, Week, Month, Quarter, Half, or Year.

## 

[​](https://docs.cfo.ai/dashboards/table-view-grammar#variables-vs-dimensions-as-rows)

Variables vs. Dimensions as rows

Each row in a table’s view is either:

- A **Variable**, which measures something (Revenue, Headcount, Gross Margin), or
- A **Dimension used as a mapping**, where each cell shows that Dimension’s item for its row and column instead of a number — useful for a database-style list of entities and their attributes.

A Variable row can carry its own breakdown, splitting just that one row differently from the rest of the table.

## 

[​](https://docs.cfo.ai/dashboards/table-view-grammar#transpose)

Transpose

By default, a view with a measured Variable keeps values on rows and its Dimensions, including time, on columns. A mapping-only view can be easier to read with items down the rows and their attributes across the columns. Ask Ari to transpose the table when that layout better matches the question.

## 

[​](https://docs.cfo.ai/dashboards/table-view-grammar#when-a-table-comes-back-empty)

When a table comes back empty

An empty result on a table with dates is almost always a **window** problem — the date range or grain the table is set to show — not a breakdown problem. Ask Ari to check the table’s window before reworking its breakdown.

## 

[​](https://docs.cfo.ai/dashboards/table-view-grammar#related)

Related

- [Build and format a Table Block](https://docs.cfo.ai/dashboards/build-and-format-tables)
- [Charts and custom visualizations](https://docs.cfo.ai/dashboards/charts-and-custom-visualizations)
- [Map one Dimension’s items to another](https://docs.cfo.ai/formulas/core-concepts/dimension-mappings)

Ctrl+I