# Source: https://docs.cfo.ai/formulas/core-concepts/variables-and-dimensions/choose-variable-or-dimension

Choose based on how people will use the field in the model.

## 

[​](https://docs.cfo.ai/formulas/core-concepts/variables-and-dimensions/choose-variable-or-dimension#use-a-variable-when)

Use a Variable when

The field:

- Represents a financial value, performance measure, assumption, or operating input.
- Is added, averaged, counted, compared, or calculated
- Belongs in the values or line-item area of a financial table
- Is a result you want a formula to produce

Examples:

- Revenue
- Cash Balance
- Headcount
- Units Sold
- Average Salary
- Gross Margin

## 

[​](https://docs.cfo.ai/formulas/core-concepts/variables-and-dimensions/choose-variable-or-dimension#use-a-dimension-when)

Use a Dimension when

The field:

- Names a category
- Groups or filters other values
- Identifies where a value belongs
- Has items people use to break down a report

Examples:

- Department
- Legal Entity
- Region
- Product
- Customer
- Vendor
- Account
- Date

## 

[​](https://docs.cfo.ai/formulas/core-concepts/variables-and-dimensions/choose-variable-or-dimension#ask-two-questions)

Ask two questions

1. Is this the value I want to measure?
2. Or is this how I want to organize that value?

If it’s the value, use a Variable. If it organizes the value, use a Dimension.

## 

[​](https://docs.cfo.ai/formulas/core-concepts/variables-and-dimensions/choose-variable-or-dimension#do-not-choose-by-data-type-alone)

Do not choose by data type alone

- Employee ID may contain numbers, but it identifies employees and is usually a Dimension.
- Gross Margin is a percentage, but it is a calculated value and is a Variable.
- Date is stored as a date, but it organizes values across time and is a Dimension.
- Headcount is a count, not a list of employees, so it is a Variable.

## 

[​](https://docs.cfo.ai/formulas/core-concepts/variables-and-dimensions/choose-variable-or-dimension#a-common-ambiguous-case-account)

A common ambiguous case: Account

A source Account or Account Code usually classifies transactions and is a Dimension. A modeled line item such as Revenue or Rent Expense is usually a Variable. If several account values roll into one modeled result, Account is the organizing Dimension and the modeled result is the Variable.

## 

[​](https://docs.cfo.ai/formulas/core-concepts/variables-and-dimensions/choose-variable-or-dimension#related)

Related

- [What is a Variable?](https://docs.cfo.ai/formulas/core-concepts/variables-and-dimensions/what-is-a-variable)
- [Segments, Dimensions, and cell addresses](https://docs.cfo.ai/formulas/core-concepts/segments-and-segmentations)

Ctrl+I