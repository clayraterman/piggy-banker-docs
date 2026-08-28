# Source: https://docs.cfo.ai/formulas/formula-reference/formula-errors-and-troubleshooting

Start with the problem you can see, then check the formula’s expression and scope.

## 

[​](https://docs.cfo.ai/formulas/formula-reference/formula-errors-and-troubleshooting#the-formula-will-not-save)

The formula will not save

Check for:

- A missing parenthesis or quote
- A Variable name that needs backticks
- A Variable that does not exist in the selected Scenario.
- An unsupported number of function arguments
- A formula range on a formula without Date scope.

## 

[​](https://docs.cfo.ai/formulas/formula-reference/formula-errors-and-troubleshooting#a-variable-cannot-be-found)

A Variable cannot be found

Use the name shown in cfo.ai. If the name contains spaces or punctuation, wrap it in backticks. If several Variables share the name, use the short disambiguator offered by the editor or Ari.

## 

[​](https://docs.cfo.ai/formulas/formula-reference/formula-errors-and-troubleshooting#the-result-is-unexpectedly-high)

The result is unexpectedly high

The formula may be selecting several values and summing them. Review lookups that use `in any`, sets, or `where`. Use an explicit aggregation when the intended result is an average, median, minimum, maximum, count, standard deviation, first value, or last value.

## 

[​](https://docs.cfo.ai/formulas/formula-reference/formula-errors-and-troubleshooting#the-formula-works-in-one-segment-but-not-another)

The formula works in one segment but not another

Check whether:

- A segment-specific formula overrides the default
- The referenced Variable exists in both segments
- An absolute reference should be a current-segment reference, or the reverse
- The table uses a different segmentation

## 

[​](https://docs.cfo.ai/formulas/formula-reference/formula-errors-and-troubleshooting#the-formula-works-in-actuals-but-not-forecast)

The formula works in Actuals but not Forecast

Check the formula range, Date scope, Date grain, Scenario, and Last close. A formula assigned to Actuals or Forecast must include Date in its scope.

## 

[​](https://docs.cfo.ai/formulas/formula-reference/formula-errors-and-troubleshooting#a-date-lookup-returns-no-value)

A date lookup returns no value

Confirm that the Date grain and value format match. A monthly lookup should use `Date.Month` and a value such as `"2026-01"`.

## 

[​](https://docs.cfo.ai/formulas/formula-reference/formula-errors-and-troubleshooting#ari-changed-only-some-formulas)

Ari changed only some formulas

Depending on the operation, a batch can apply valid changes while rejecting invalid ones, or reject the whole batch when all changes must succeed together. Ask Ari which changes were applied, fix the reported issue, and verify the resulting values.

## 

[​](https://docs.cfo.ai/formulas/formula-reference/formula-errors-and-troubleshooting#a-division-returns-an-error)

A division returns an error

Division by zero produces a calculation error. Guard the divisor or provide a fallback:

```
iferror(`Gross Profit` / Revenue, 0)
```

## 

[​](https://docs.cfo.ai/formulas/formula-reference/formula-errors-and-troubleshooting#related)

Related

- [Formula syntax and operators](https://docs.cfo.ai/formulas/formula-reference/formula-syntax-and-operators)
- [Aggregation functions](https://docs.cfo.ai/formulas/formula-reference/function-reference/aggregation-functions)

Ctrl+I