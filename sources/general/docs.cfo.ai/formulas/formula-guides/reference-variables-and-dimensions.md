# Source: https://docs.cfo.ai/formulas/formula-guides/reference-variables-and-dimensions

A formula can use other Variables as inputs. Write Variable names the same way they appear in cfo.ai.

## 

[​](https://docs.cfo.ai/formulas/formula-guides/reference-variables-and-dimensions#plain-references)

Plain references

A plain name reads the Variable in the current segment:

```
Revenue
```

If the formula is calculating a result for Sales, `Revenue` reads Sales Revenue. If it is calculating a result for West, it reads West Revenue. These three forms read the same current-segment value:

```
Revenue
this.Revenue
Revenue[]
```

## 

[​](https://docs.cfo.ai/formulas/formula-guides/reference-variables-and-dimensions#names-with-spaces-or-punctuation)

Names with spaces or punctuation

Wrap a name in backticks when it contains spaces, punctuation, an operator, or a reserved word:

```
`Cost of Goods Sold`
```

Example:

```
Revenue - `Cost of Goods Sold`
```

## 

[​](https://docs.cfo.ai/formulas/formula-guides/reference-variables-and-dimensions#a-specific-segment)

A specific segment

Use brackets to replace one part of the current segment:

```
Revenue[Region = "West"]
```

Other dimensions still follow the current segment.

## 

[​](https://docs.cfo.ai/formulas/formula-guides/reference-variables-and-dimensions#an-absolute-reference)

An absolute reference

Place `$` immediately after the Variable name when the lookup should not inherit the current segment:

```
Revenue$
```

You can combine an absolute reference with explicit filters:

```
Revenue$[Region = "West"]
```

Use absolute references carefully. Most formulas should follow the segment they are calculating.

## 

[​](https://docs.cfo.ai/formulas/formula-guides/reference-variables-and-dimensions#duplicate-names)

Duplicate names

If two Variables have the same name, cfo.ai adds a short disambiguator:

```
Revenue#a3f
```

Use the shortest disambiguator offered by the editor or Ari.

## 

[​](https://docs.cfo.ai/formulas/formula-guides/reference-variables-and-dimensions#date-granularity)

Date granularity

Add a granularity to Date when the formula works with time buckets:

```
Date.Month
```

Supported grains are Day, Week, Month, Quarter, Half, and Year.

## 

[​](https://docs.cfo.ai/formulas/formula-guides/reference-variables-and-dimensions#previous-and-next-periods)

Previous and next periods

Use a signed offset after a Variable to read a nearby period:

```
Revenue[-1]
Revenue[1]
```

At a monthly grain, `Revenue[-1]` reads the previous month. The same expression follows the current Date grain.

## 

[​](https://docs.cfo.ai/formulas/formula-guides/reference-variables-and-dimensions#related)

Related

- [Filter by Dimension items](https://docs.cfo.ai/formulas/formula-guides/filter-by-dimension-items)
- [Work with dates](https://docs.cfo.ai/formulas/formula-guides/work-with-dates)

Ctrl+I