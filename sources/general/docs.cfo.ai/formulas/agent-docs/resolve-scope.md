# Source: https://docs.cfo.ai/formulas/agent-docs/resolve-scope

Formula scope determines which Model values a saved rule controls. A visible Table Block target is the preferred authority because the server can derive the actual cell address and formula range.

## 

[​](https://docs.cfo.ai/formulas/agent-docs/resolve-scope#start-from-the-visible-target)

Start from the visible target

Inspect the relevant saved table and copy the returned row or column reference into `edit_table_blocks`. Use a row or column for a rule that applies along that axis, or a cell for one exact visible result. The server derives scope from the target. The caller does not invent Dimension IDs, array positions, or formula-range IDs.

## 

[​](https://docs.cfo.ai/formulas/agent-docs/resolve-scope#model-wide-default)

Model-wide default

The broad default condition is:

```
[]
```

Use it when the same rule should apply across the Model and no narrower business condition is intended.

## 

[​](https://docs.cfo.ai/formulas/agent-docs/resolve-scope#a-rule-for-a-dimension)

A rule for a Dimension

A rule for every Department item uses:

```
[Department in any]
```

The unprefixed condition continues to apply when additional Dimensions are present.

## 

[​](https://docs.cfo.ai/formulas/agent-docs/resolve-scope#a-rule-for-one-segment)

A rule for one segment

Use the readable Dimension and item names returned by inspection:

```
[Department = "Sales"]
```

```
[Department = "Sales", Region = "West"]
```

Wrap names with spaces in backticks and use a returned short disambiguator only when needed.

## 

[​](https://docs.cfo.ai/formulas/agent-docs/resolve-scope#time-aware-scope)

Time-aware scope

A formula range needs the Model’s Date grain. In a monthly Model:

```
[Department = "Sales", Date.Month in any]
```

For a table-independent `edit_variables` write, pair the condition with the requested `period`, such as `"forecast"`, when the rule belongs to that formula range.

## 

[​](https://docs.cfo.ai/formulas/agent-docs/resolve-scope#exact-versus-broader-scope)

Exact versus broader scope

A condition without `$` can continue to match a richer cell address. A condition beginning with `$` matches the exact set of Dimensions it names:

```
[Department = "Sales"]
$[Department = "Sales"]
```

For a table-independent write, pass the exact condition directly in the supported `condition` field:

```
{
  "condition": "$[Department = \"Sales\"]"
}
```

The leading `$` is part of the condition grammar. In an expression, an absolute Variable reference instead places `$` after its name: `Revenue$[Department = "Sales"]`. Use exact scope only when the user intends that narrower behavior. A rule that omits Date cannot fill dated cells if it matches only its exact Dimension set.

Ctrl+I