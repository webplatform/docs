---
title: 'column-rule-style'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/6288958'
compatibility:
  feature: column-rule-style
  topic: css
notes:
  - 'Add description, compatibility.'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`none`'
  'Applies to': 'multi-column elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'specified value'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`columnRuleStyle`'
  Percentages: N/A
readiness: 'In Progress'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Specifies the style of the rule between columns. The column-rule-style values are the same as for border-style.'
tags:
  - CSS
  - Properties
uri: css/properties/column-rule-style

---
## Summary

Specifies the style of the rule between columns. The column-rule-style values are the same as for border-style.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `none`

Applies to
:   multi-column elements

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   specified value

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `columnRuleStyle`

Percentages
:   N/A

## Syntax

-   `column-rule-style: dashed`
-   `column-rule-style: dotted`
-   `column-rule-style: double`
-   `column-rule-style: groove`
-   `column-rule-style: hidden`
-   `column-rule-style: inset`
-   `column-rule-style: none`
-   `column-rule-style: outset`
-   `column-rule-style: ridge`
-   `column-rule-style: solid`

## Values

none
:   Default. No column rule is drawn, regardless of any specified `column-rule-width`. The computed value is set to 0.

dotted
:   Column rule is a dotted line.

dashed
:   Column rule is a dashed line.

solid
:   Column rule is a solid line.

double
:   Column rule is two parallel solid lines with a space between. The sum of the two single lines and the space between equals the `column-rule-width` value. The column rule width must be at least 3 pixels wide to draw a double rule.

groove
:   3-D groove is drawn in colors slightly lighter and darker than the value.

ridge
:   3-D ridge is drawn in colors based on the value.

inset
:   3-D inset is drawn in colors based on the value.

outset
:   3-D outset is drawn in colors based on the value.

hidden
:   Same as `none`.

## Examples

Makes 3 columns with 4px dashed green column-rule.

``` css
/*
Makes 3 columns with 4px dashed green column-rule
*/

#columns {
  columns: 3;

  /* Prefix free example below, use vendor prefixes where needed */
  column-rule-style: dashed;
  column-rule-color: green;
  column-rule-width: 5px;
}
```

[View live example](http://code.webplatform.org/gist/6288958)

## Related specifications

[CSS Multi-column Layout Module](http://www.w3.org/TR/css3-multicol/)
:   W3C Candidate Recommendation

## See also

### Related articles

#### Multi-Column

-   [break-after](/css/properties/break-after)

-   [break-before](/css/properties/break-before)

-   [break-inside](/css/properties/break-inside)

-   [column-count](/css/properties/column-count)

-   [column-gap](/css/properties/column-gap)

-   [column-rule](/css/properties/column-rule)

-   [column-rule-color](/css/properties/column-rule-color)

-   **column-rule-style**

-   [column-rule-width](/css/properties/column-rule-width)

-   [column-span](/css/properties/column-span)

-   [column-width](/css/properties/column-width)

-   [content](/css/properties/content)
