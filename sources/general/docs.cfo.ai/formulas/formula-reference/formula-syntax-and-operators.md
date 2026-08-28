# Source: https://docs.cfo.ai/formulas/formula-reference/formula-syntax-and-operators

Use this page to look up the building blocks of a formula.

## 

[​](https://docs.cfo.ai/formulas/formula-reference/formula-syntax-and-operators#numbers-and-percentages)

Numbers and percentages

```
1000
1000.5
.5
50%
```

`50%` is the same as `0.5`. A minus sign can make a value negative.

## 

[​](https://docs.cfo.ai/formulas/formula-reference/formula-syntax-and-operators#arithmetic)

Arithmetic

- `+` add
- `-` subtract
- `*` multiply
- `/` divide
- `%` remainder
- `^` power

Example:

```
Price * Quantity
```

Power chains are evaluated from the right. Use parentheses when the order matters.

## 

[​](https://docs.cfo.ai/formulas/formula-reference/formula-syntax-and-operators#comparisons)

Comparisons

- `=` equal
- `<>` not equal
- `>` greater than
- `<` less than
- `>=` greater than or equal
- `<=` less than or equal

## 

[​](https://docs.cfo.ai/formulas/formula-reference/formula-syntax-and-operators#logical-operators)

Logical operators

Use `and`, `or`, and `not`.

```
Revenue > 0 and `Cost of Goods Sold` > 0
```

## 

[​](https://docs.cfo.ai/formulas/formula-reference/formula-syntax-and-operators#variable-names)

Variable names

```
Revenue
`Net Revenue`
Revenue#a3f
```

Backticks protect names with spaces or punctuation. A short `#` suffix distinguishes duplicate names.

## 

[​](https://docs.cfo.ai/formulas/formula-reference/formula-syntax-and-operators#segment-lookups)

Segment lookups

```
Revenue[Department = "Sales"]
Revenue[Department in {"Sales", "Marketing"}]
Revenue[Department not in {"Engineering"}]
Revenue[Department in any]
```

A plain lookup inherits the rest of the current segment. Put `$` after the Variable name for an absolute lookup:

```
Revenue$
Revenue$[Department = "Sales"]
```

## 

[​](https://docs.cfo.ai/formulas/formula-reference/formula-syntax-and-operators#relative-period-references)

Relative period references

```
Revenue[-1]
Revenue[1]
Revenue[Department = "Sales"][-1]
```

An offset follows the current Date grain. In a monthly calculation, `Revenue[-1]` refers to the previous month.

## 

[​](https://docs.cfo.ai/formulas/formula-reference/formula-syntax-and-operators#date-references)

Date references

```
Date.Day
Date.Week
Date.Month
Date.Quarter
Date.Half
Date.Year
```

## 

[​](https://docs.cfo.ai/formulas/formula-reference/formula-syntax-and-operators#formula-conditions)

Formula conditions

Conditions describe where a saved formula applies:

```
[]
[Department in any]
[Department = "Sales"]
[Department = "Sales", Date.Month in any]
$[Department = "Sales"]
$[]
```

`[]` applies broadly across the Model. An unprefixed condition such as `[Department = "Sales"]` continues to match when other Dimensions are present. `$[Department = "Sales"]` matches exactly the named Dimension set, while `$[]` matches only the empty segmentation. The leading `$` belongs to a saved formula condition. In an expression, an absolute Variable reference instead places `$` after its name, as in `Revenue$[Department = "Sales"]`. Most users choose scope through the formula editor or tell Ari where the rule should apply.

## 

[​](https://docs.cfo.ai/formulas/formula-reference/formula-syntax-and-operators#function-calls)

Function calls

Write functions with their supported lowercase names:

```
sum(Revenue[Department in any])
average(Revenue[Department in any])
iferror(`Gross Profit` / Revenue, 0)
dateadd(Date.Month, -1, "month")
```

See the function reference for the full supported catalog and argument counts.

## 

[​](https://docs.cfo.ai/formulas/formula-reference/formula-syntax-and-operators#preferred-spellings)

Preferred spellings

Use `^`, `=`, and `<>` in new formulas. Older formulas may contain `**`, `==`, or `!=`; those spellings remain accepted. Use the syntax shown on this page for new formulas. If an older expression is unclear, ask Ari to explain or update it using the current supported form.

Ctrl+I