# Source: https://docs.cfo.ai/getting-started/build-your-financial-model

A useful financial Model is a dynamic simulation of how your business works. Change a hiring date, growth assumption, or price, and you can see how the decision affects revenue, expenses, and cash over time. You and Ari work from the same Model. Ari can build or update it, and you can inspect the formulas, change assumptions, and keep using the result after the conversation ends.

## 

[​](https://docs.cfo.ai/getting-started/build-your-financial-model#start-with-how-the-business-works)

Start with how the business works

Identify the real things and events that change your results.

- A subscription company may need customers, plans, seats, new contracts, expansion, churn, billing, and collections.
- A services business may need clients, projects, team members, billable time, utilization, and project start and end dates.
- A retail or physical-product business may need products, orders, inventory, purchase timing, fulfillment, and returns.

Tell Ari what creates revenue, what creates cost, and what decisions the Model should help you make.

> We sell annual software subscriptions. Model customers by segment and plan, include new business and churn, and connect hiring and operating expenses to our cash forecast.

## 

[​](https://docs.cfo.ai/getting-started/build-your-financial-model#keep-meaningful-business-detail)

Keep meaningful business detail

Use Dimensions for the categories that change how you analyze the business. Common examples include Customer, Product, Department, Employee, Region, Entity, and Date. The right level of detail depends on the decision. If churn differs by customer segment, keep customer segment. If payroll depends on a person’s start date, compensation, and department, keep the employee-level detail behind the department total. One real business category should map to one shared Dimension wherever possible. For example, Department should mean the same thing when data comes from accounting and HR.

## 

[​](https://docs.cfo.ai/getting-started/build-your-financial-model#connect-source-data-and-assumptions)

Connect source data and assumptions

Actuals come from the accounting, HR, CRM, spreadsheet, database, or file sources you connect. Assumptions describe what should happen next when the future cannot be observed directly. Useful assumptions are named, visible, and easy to change. Examples include conversion rate, planned hiring, price increases, payment timing, and monthly churn. When source data is incomplete, Ari can still build a forecast from explicit assumptions. Ask Ari to identify which values came from a source and which values were assumed.

## 

[​](https://docs.cfo.ai/getting-started/build-your-financial-model#make-time-part-of-the-model)

Make time part of the model

Every business changes across time. Set the date range and grain that match the question, such as months for a 12-month operating plan or weeks for a near-term cash forecast. **Last close** separates closed Actuals from the Forecast. A Variable can use imported data in Actuals and a planning formula in Forecast while keeping the same business meaning across both ranges. For example:

```
`Ending Customers` = `Beginning Customers` + `New Customers` - `Churned Customers`
```

```
`Subscription Revenue` = Customers * `Average Subscription Price`
```

The `=` in these examples explains the business relationship. When entering a formula for a selected Variable, enter the expression to the right of `=`.

## 

[​](https://docs.cfo.ai/getting-started/build-your-financial-model#build-one-connected-system)

Build one connected system

Revenue, headcount, expenses, balance-sheet activity, and cash should agree with each other. A hiring plan should affect payroll. Changes in sales should affect recognized revenue and collections. The cash forecast should reflect the timing of the underlying inflows and outflows. The same Model can appear in a hiring plan, cash forecast, or board report without becoming three disconnected copies. A business value keeps its meaning wherever you or Ari inspect it. Organize the results into Pages and Table Blocks, then ask Ari to verify that important totals reconcile across the Model.

> Check that the department payroll totals match the employee detail, and show how the hiring plan changes ending cash.

## 

[​](https://docs.cfo.ai/getting-started/build-your-financial-model#test-decisions-in-a-scenario)

Test decisions in a Scenario

Keep Main as your working baseline. Create a Scenario when you want to explore a different price, growth rate, hiring plan, or financing decision without changing that baseline.

> Create a Scenario where enterprise churn falls by two percentage points and show the effect on revenue and cash over the next year.

## 

[​](https://docs.cfo.ai/getting-started/build-your-financial-model#related)

Related

- [Understand the formula model](https://docs.cfo.ai/formulas/get-started/understand-the-formula-model)
- [Connect and sync your data](https://docs.cfo.ai/integrations/connect-and-sync-data)
- [Create and compare Scenarios](https://docs.cfo.ai/scenarios/create-and-compare-scenarios)
- [Build a Headcount page](https://docs.cfo.ai/headcount/build-a-headcount-page)

Ctrl+I