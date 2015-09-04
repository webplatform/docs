---
title: column-width
tags:
  - CSS
  - Properties
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Specifies the width of columns in multi-column elements.'
code_samples:
  - 'http://gist.github.com/5305475'
uri: css/properties/column-width

---
# column-width

## Summary

Specifies the width of columns in multi-column elements.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `auto`
Applies to
:   non-replaced block-level elements (except table elements), table cells, and inline-block elements
[Inherited](/css/concepts/inherited)
:   No
Media
:   visual
[Computed value](/css/concepts/computed_value)
:   the absolute length, zero or larger
Animatable
:   Yes
[CSS Object Model Property](/css/concepts/cssom)
:   `columnWidth`
Percentages
:   N/A

## Syntax

-   `column-width: auto`
-   `column-width: length`

## Values

length
:   A floating-point number, followed by either an absolute units designator

(`cm`, `mm`, `in`, `pt`, or `pc`) or a relative units designator (`rem`, `em`, `ex`, or `px`), that indicates the optimal width. For more information about the supported length units, see CSS Length Units Reference.

auto
:   Default. The optimal column width is determined through other property values of the multi-column element, such as [**columnCount**](/css/properties/column-count).

## Examples

Makes as many columns that are 100px as there is space in the browser.

``` {.css}
/*
Makes as many columns that are 100px as there is space in the browser.
*/

#column {
  /* Prefix free example below, use vendor prefixes where needed */
  column-width: 100px;
}
```

[View live example](http://code.webplatform.org/gist/5305475)

## Notes

### Remarks

The actual column width may vary from the value specified due to available space. To ensure that the exact value specified for this property is used, all property values of the multi-column element that pertain to length (such as width, column-width, column-gap, and column-rule-width) must be specified.

## Related specifications

Specification
:   Status
[CSS Multi-column Layout Module](http://www.w3.org/TR/css3-multicol/)
:   Candidate Recommendation

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

-   [column-rule-style](/css/properties/column-rule-style)

-   [column-rule-width](/css/properties/column-rule-width)

-   [column-span](/css/properties/column-span)

-   **column-width**

-   [content](/css/properties/content)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

