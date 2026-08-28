# Source: https://docs.cfo.ai/formulas/get-started/write-your-first-formula

Start with a calculation your team can recognize: Gross Profit equals Revenue minus Cost of Goods Sold.

## 

[​](https://docs.cfo.ai/formulas/get-started/write-your-first-formula#before-you-begin)

Before you begin

You need a target Variable and the Variables it will reference. In this example:

- Target Variable: Gross Profit
- Referenced Variables: Revenue and Cost of Goods Sold

## 

[​](https://docs.cfo.ai/formulas/get-started/write-your-first-formula#1-open-the-target-variable)

1\. Open the target Variable

Open **Gross Profit** and go to its formula editor. The formula belongs to Gross Profit because that is the value it calculates.

## 

[​](https://docs.cfo.ai/formulas/get-started/write-your-first-formula#2-enter-the-calculation)

2\. Enter the calculation

Write:

```
Revenue - `Cost of Goods Sold`
```

Use the Variable names shown in cfo.ai. Wrap names that contain spaces, punctuation, operators, or reserved words in backticks.

## 

[​](https://docs.cfo.ai/formulas/get-started/write-your-first-formula#3-choose-where-it-applies)

3\. Choose where it applies

For a first formula, use the broadest appropriate scope so it acts as the default calculation for the Variable. You can add a more specific formula later for a Dimension, a segment, Actuals, or Forecast.

## 

[​](https://docs.cfo.ai/formulas/get-started/write-your-first-formula#4-check-the-formula)

4\. Check the formula

Before saving, confirm that:

- Gross Profit is the target Variable
- Revenue and Cost of Goods Sold are the intended inputs
- The formula applies in the intended Scenario.
- The scope is not more specific than you need

cfo.ai validates the syntax and Variable references when the formula is saved.

## 

[​](https://docs.cfo.ai/formulas/get-started/write-your-first-formula#5-review-the-result)

5\. Review the result

Open a Table Block that contains Gross Profit. Check a few periods and, if the table is segmented, a few Dimension items. For example, if Revenue is 100 and Cost of Goods Sold is 40, Gross Profit should be 60.

## 

[​](https://docs.cfo.ai/formulas/get-started/write-your-first-formula#add-detail-when-you-need-it)

Add detail when you need it

Once the default formula works, you can add a more specific formula without changing the default everywhere. Common next steps include:

- Calculate Gross Profit differently for one department
- Use a different formula in Forecast
- Reference another period
- Aggregate several Dimension items.

Use [Choose where a formula applies](https://docs.cfo.ai/formulas/core-concepts/choose-where-a-formula-applies) before adding an override.

## 

[​](https://docs.cfo.ai/formulas/get-started/write-your-first-formula#ask-ari-instead)

Ask Ari instead

You can also describe the same outcome:

> Add Gross Profit to this table, calculate it as Revenue minus Cost of Goods Sold, and check the result for the last three months.

Ari can add the visible row, save the calculation, and inspect the resulting values.

Ctrl+I