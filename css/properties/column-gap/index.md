---
title: 'column-gap'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://code.webplatform.org/gist/5305647'
compatibility:
  feature: column-gap
  topic: css
notes:
  - 'Add description, compatibility.'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`normal`'
  'Applies to': 'multi-column elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'absolute length or ‘normal’'
  Animatable: 'Yes'
  '[CSS Object Model Property](/css/concepts/cssom)': '`columnGap`'
  Percentages: N/A
readiness: 'In Progress'
standardization_status: 'W3C Candidate Recommendation'
summary: 'The column-gap property controls the width of the gap between columns in multi-column elements.'
tags:
  - CSS_Properties
  - CSS
uri: css/properties/column-gap

---
## Summary

The column-gap property controls the width of the gap between columns in multi-column elements.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `normal`

Applies to
:   multi-column elements

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   absolute length or ‘normal’

Animatable
:   Yes

[CSS Object Model Property](/css/concepts/cssom)
:   `columnGap`

Percentages
:   N/A

## Syntax

-   `column-gap: length`
-   `column-gap: normal`

## Values

normal
:   Default. The width of the `normal` value is user-agent specific, but `1em` is suggested.

length
:   A floating-point number, followed by either an absolute units designator

(`cm`, `mm`, `in`, `pt`, or `pc`) or a relative units designator (`em`, `ex`, or `px`), that indicates the width of the gap between columns. For more information about the supported length units, see CSS Length Units Reference.

 Negative values are not valid.

## Examples

Makes as many 15em columns with a column-gap of 4em

``` css
/*
Makes as many 15em columns with a column-gap of 4em
*/

#columns {
  /* Prefix free example below, use vendor prefixes where needed */
  column-width: 15em;
  column-gap: 4em;
  column-rule: 1px solid green;
}
```

[View live example](http://code.webplatform.org/gist/5305647)

## Related specifications

[CSS Multi-column Layout Module](http://www.w3.org/TR/css3-multicol/)
:   Candidate Recommendation

## See also

### Related articles

#### Multi-Column

-   [break-after](/css/properties/break-after)

-   [break-before](/css/properties/break-before)

-   [break-inside](/css/properties/break-inside)

-   [column-count](/css/properties/column-count)

-   **column-gap**

-   [column-rule](/css/properties/column-rule)

-   [column-rule-color](/css/properties/column-rule-color)

-   [column-rule-style](/css/properties/column-rule-style)

-   [column-rule-width](/css/properties/column-rule-width)

-   [column-span](/css/properties/column-span)

-   [column-width](/css/properties/column-width)

-   [content](/css/properties/content)
