# Source: https://docs.cfo.ai/formulas/core-concepts/segments-and-segmentations

Dimensions organize Model values into meaningful business categories. A segment is the slice of a Variable identified by one or more Dimension items.

## 

[​](https://docs.cfo.ai/formulas/core-concepts/segments-and-segmentations#dimensions-and-their-items)

Dimensions and their items

A Dimension defines a category, and its items identify the entries within that category.

- Department might contain Sales, Engineering, and Marketing.
- Region might contain East and West.
- Product might contain Starter and Enterprise.

## 

[​](https://docs.cfo.ai/formulas/core-concepts/segments-and-segmentations#a-segment-belongs-to-a-variable)

A segment belongs to a Variable

A segment is a slice of a Variable’s data:

- Revenue for Sales.
- Revenue for the West.
- Revenue for Sales in the West.

Sales is a Dimension item. Revenue for Sales is the segment. Several Dimensions can describe the same segment when the question needs more detail.

## 

[​](https://docs.cfo.ai/formulas/core-concepts/segments-and-segmentations#a-cell-address-identifies-one-result)

A cell address identifies one result

A cell address identifies a Variable, one item from each applicable Dimension, and a time period. For example:

> Revenue for Sales in the West for March 2026.

That address is more precise than a segment because it also identifies the exact period and every Dimension needed for that cell.

## 

[​](https://docs.cfo.ai/formulas/core-concepts/segments-and-segmentations#show-segments-in-a-table-block)

Show segments in a Table Block

Use **Segment by** when you want a Table Block to expose a Variable’s segments by another Dimension. For example, segment Revenue by Department to see Sales, Engineering, and Marketing separately. The **Segmentation** option in the **Use as** control identifies a Dimension’s display role. A Dimension used as **Mapping** instead shows its item as a cell value.

## 

[​](https://docs.cfo.ai/formulas/core-concepts/segments-and-segmentations#formula-scope-follows-the-business-rule)

Formula scope follows the business rule

A default formula can apply broadly. A more specific formula can apply when a Variable is segmented by Department, or only when Department is Sales. Start with the broadest rule that expresses the actual business behavior. Add a segment-specific formula only when that segment genuinely needs a different calculation.

## 

[​](https://docs.cfo.ai/formulas/core-concepts/segments-and-segmentations#related)

Related

- [Choose where a formula applies](https://docs.cfo.ai/formulas/core-concepts/choose-where-a-formula-applies)
- [Build and format a Table Block](https://docs.cfo.ai/dashboards/build-and-format-tables)
- [Glossary and key concepts](https://docs.cfo.ai/glossary)

Ctrl+I