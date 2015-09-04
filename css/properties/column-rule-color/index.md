---
title: column-rule-color
tags:
  - CSS
  - Properties
readiness: 'In Progress'
standardization_status: 'W3C Candidate Recommendation'
notes:
  - 'Add description, compatibility.'
summary: 'Specifies the color of the rule between columns.'
code_samples:
  - 'http://gist.github.com/6288958'
uri: css/properties/column-rule-color

---
# column-rule-color

## Summary

Specifies the color of the rule between columns.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `currentColor (same as for ‘color’ property)`
Applies to
:   multi-column elements
[Inherited](/css/concepts/inherited)
:   No
Media
:   visual
[Computed value](/css/concepts/computed_value)
:   as specified
Animatable
:   Yes
[CSS Object Model Property](/css/concepts/cssom)
:   `columnRuleColor`
Percentages
:   N/A

## Syntax

-   `column-rule-color: color`

## Values

color
:   One of the color names, RGB, RGBA, HSL, or HSLA values in the [Color Table](/css/color/color_table).

## Examples

Uses the column-rule-color property to set the color of the rule between columns.

``` {.css}
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

Specification
:   Status
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

-   **column-rule-color**

-   [column-rule-style](/css/properties/column-rule-style)

-   [column-rule-width](/css/properties/column-rule-width)

-   [column-span](/css/properties/column-span)

-   [column-width](/css/properties/column-width)

-   [content](/css/properties/content)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

