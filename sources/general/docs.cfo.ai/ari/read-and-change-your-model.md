# Source: https://docs.cfo.ai/ari/read-and-change-your-model

Ari can inspect existing information or change the Model on your behalf. The right behavior depends on whether you asked for an explanation, a review, or a saved result.

## 

[​](https://docs.cfo.ai/ari/read-and-change-your-model#read-existing-information)

Read existing information

Questions about a Page, Table Block, Variable, Scenario, source, or previous change can often be answered from what already exists.

> What changed in operating expenses since last month?

> Which formula calculates Payroll for Sales in Forecast?

> Has the accounting integration finished loading?

Reading existing information does not create or modify Model content.

## 

[​](https://docs.cfo.ai/ari/read-and-change-your-model#review-a-proposed-change)

Review a proposed change

You can ask Ari to explain a proposed formula or validate a supported write before applying it.

> Draft a formula for gross margin and tell me whether it is valid. Do not save it yet.

Validation checks the proposed rule. It does not create a new calculated series in your Model.

## 

[​](https://docs.cfo.ai/ari/read-and-change-your-model#save-a-visible-model-change)

Save a visible Model change

Requests to create, update, delete, schedule, or reorganize content can change your workspace. Examples include creating a Scenario, adding a Variable to a Table Block, saving a formula, or updating an assumption.

> Add Gross Margin to the revenue table and calculate it as gross profit divided by revenue.

When a new calculation must be evaluated, Ari creates or reuses a visible Model row and reads the result from the saved Table Block. That makes the calculation inspectable and available for later follow-up.

## 

[​](https://docs.cfo.ai/ari/read-and-change-your-model#protect-your-baseline)

Protect your baseline

Use a Scenario when you want to test a saved change while keeping Main unchanged.

> Create an Upside Scenario, increase the enterprise conversion assumption, and compare the result with Main.

For a destructive or broad change, ask Ari to explain the effect before it applies the change. If something lands incorrectly, ask Ari to review the history and help you undo or revert the affected work.

## 

[​](https://docs.cfo.ai/ari/read-and-change-your-model#related)

Related

- [Explore existing calculations without saving](https://docs.cfo.ai/formulas/work-with-ari/explore-calculations-without-saving)
- [Ask Ari to create or update formulas](https://docs.cfo.ai/formulas/work-with-ari/ask-ari-to-create-or-update-formulas)
- [Understand Scenarios](https://docs.cfo.ai/scenarios/understand-scenarios)

Ctrl+I