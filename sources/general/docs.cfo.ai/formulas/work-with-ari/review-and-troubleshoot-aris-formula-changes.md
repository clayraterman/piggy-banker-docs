# Source: https://docs.cfo.ai/formulas/work-with-ari/review-and-troubleshoot-aris-formula-changes

After Ari writes a formula, review the formula card and the calculated result.

## 

[​](https://docs.cfo.ai/formulas/work-with-ari/review-and-troubleshoot-aris-formula-changes#review-the-formula-card)

Review the formula card

Check:

- **Variable:** Is this the Variable you meant to change?
- **Expression:** Does it describe the intended business rule?
- **Scope:** Does it apply everywhere, to a Dimension, or to a specific segment?
- **Formula range:** Does it apply to Actuals, Forecast, or both?
- **Scenario:** Was it written to the intended scenario?

## 

[​](https://docs.cfo.ai/formulas/work-with-ari/review-and-troubleshoot-aris-formula-changes#ask-ari-to-verify-the-result)

Ask Ari to verify the result

> Check the resulting values in the P&L table and compare them with Revenue minus Cost of Goods Sold.

> Verify this formula for Sales and Engineering for the next three months.

A successful save confirms that the formula is valid. Checking calculated values confirms that its business behavior is also correct.

## 

[​](https://docs.cfo.ai/formulas/work-with-ari/review-and-troubleshoot-aris-formula-changes#diagnose-before-changing)

Diagnose before changing

If a result is unexpected, ask Ari to inspect the current formulas first:

> Explain why this formula works for Sales but not Marketing. Do not change anything yet.

> Check whether a more specific formula is overriding this one.

> Check whether this lookup returns several values and needs an aggregation.

> Explain why this formula cannot be assigned only to Forecast.

## 

[​](https://docs.cfo.ai/formulas/work-with-ari/review-and-troubleshoot-aris-formula-changes#correct-a-formula)

Correct a formula

Once the cause is clear, describe the intended correction and scope. Ask Ari to validate, write, and verify the revised formula. For several changes at once, ask which items were applied and whether any were rejected. Confirm the final values instead of assuming that a successful-looking response proves the financial result is correct.

Ctrl+I