# Source: https://docs.cfo.ai/formulas/core-concepts/choose-where-a-formula-applies

A formula’s scope determines where it is used. Choose the broadest scope that matches the business rule.

## 

[​](https://docs.cfo.ai/formulas/core-concepts/choose-where-a-formula-applies#default-formula)

Default formula

A default formula is the fallback calculation for a Variable. Use it when the same business rule should apply across the model. Example: Gross Profit is Revenue minus Cost of Goods Sold everywhere. The broad default condition is:

```
[]
```

## 

[​](https://docs.cfo.ai/formulas/core-concepts/choose-where-a-formula-applies#formula-for-a-dimension)

Formula for a Dimension

A Dimension-specific formula applies when the Variable is calculated using that Dimension. Example: calculate an allocation differently whenever Expense is broken down by Department. A rule for every Department can be represented as:

```
[Department in any]
```

This rule matches Department as a whole. It does not pick only Sales or Engineering.

## 

[​](https://docs.cfo.ai/formulas/core-concepts/choose-where-a-formula-applies#segment-formula)

Segment formula

A segment formula applies to a specific Dimension item or combination of items. Examples:

- Department = Sales
- Region = West
- Department = Sales and Region = West

For example:

```
[Department = "Sales"]
```

Use segment formulas for real exceptions. If every department needs the same expression, use one broader rule instead of creating a separate formula for every item.

## 

[​](https://docs.cfo.ai/formulas/core-concepts/choose-where-a-formula-applies#formula-range)

Formula range

A formula can also be limited to a formula range such as Actuals or Forecast. Formula ranges use Date, so a range-specific formula must include the Model’s Date grain in its scope. For a monthly Model:

```
[Date.Month in any]
```

## 

[​](https://docs.cfo.ai/formulas/core-concepts/choose-where-a-formula-applies#combining-scopes)

Combining scopes

Scopes can be combined. For example, a formula can apply only to Sales during Forecast. For example:

```
[Department = "Sales", Date.Month in any]
```

Assign that rule to Forecast when it should apply only to Sales in future periods. Broader formulas remain available everywhere the specific rule does not match.

## 

[​](https://docs.cfo.ai/formulas/core-concepts/choose-where-a-formula-applies#related)

Related

- [Actuals, Forecast, and formula ranges](https://docs.cfo.ai/formulas/core-concepts/actuals-forecast-and-formula-ranges)
- [How cfo.ai chooses a formula](https://docs.cfo.ai/formulas/core-concepts/how-cfoai-chooses-a-formula)

Ctrl+I