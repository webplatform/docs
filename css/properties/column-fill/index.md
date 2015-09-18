---
title: 'column-fill'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/hh772197(v=vs.85).aspx)'
code_samples:
  - 'http://code.webplatform.org/gist/6393571'
compatibility:
  feature: column-fill
  topic: css
notes:
  - 'Complete summery, compatibility.'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`balance`'
  'Applies to': 'multi-column elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'As specified'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
readiness: 'In Progress'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Specifies how to fill columns (balanced or sequential).'
tags:
  - CSS_Properties
  - CSS
uri: css/properties/column-fill

---
## Summary

Specifies how to fill columns (balanced or sequential).

## Overview table

[Initial value](/css/concepts/initial_value)
:   `balance`

Applies to
:   multi-column elements

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   As specified

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:

## Syntax

-   `column-fill: auto`
-   `column-fill: balance`

## Values

balance
:   Columns are filled sequentially such that the column heights are balanced as equally as possible, depending on other column property values.

auto
:   Columns are filled sequentially such that the columns may differ in length, depending on other column property values.

## Examples

``` css
/*
Make as many 15em columns as possible
but restrict the heights of the columns to 400px
with column-fill: balance;
*/

#columns {
  /* Prefix free example below, use vendor prefixes where needed */
  column-width: 15em;
  column-fill: balance;
  height: 400px;
}
```

[View live example](http://code.webplatform.org/gist/6393571)

## Notes

In continuous media, this property will only be consulted if the length of columns has been constrained. Otherwise, columns will automatically be balanced.

In continous media, this property does not have any effect in overflow columns; in paged media, this property will only have effect on the last page the multicol element appears on.

Column balancing is also dependent on the values of [orphans](/css/properties/orphans) and [widows](/css/properties/widows), if set.

## Related specifications

[CSS Multi-column Layout Module](http://www.w3.org/TR/css3-multicol/)
:   W3C Candidate Recommendation
