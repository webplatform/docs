---
title: 'column-count'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/hh772195(v=vs.85).aspx)'
code_samples:
  - 'http://gist.github.com/6288917'
compatibility:
  feature: column-count
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`auto`'
  'Applies to': 'non-replaced block-level elements (except table elements), table cells, and inline-block elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'as specified'
  Animatable: 'Yes'
  '[CSS Object Model Property](/css/concepts/cssom)': '`columnCount`'
  Percentages: N/A
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Specifies the number of columns an element should be divided into.'
tags:
  - CSS
  - Properties
uri: css/properties/column-count

---
## Summary

Specifies the number of columns an element should be divided into.

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
:   as specified

Animatable
:   Yes

[CSS Object Model Property](/css/concepts/cssom)
:   `columnCount`

Percentages
:   N/A

## Syntax

-   `column-count: auto`
-   `column-count: count`

## Values

count
:   An integer value that specifies the number of columns in the multi-column element. Values must be greater than 0. When [**column-width**](/css/properties/column-width) is specified with ****column-count**** and both have non-auto values, the integer value defines the maximum number of columns.

auto
:   The number of columns is determined by the values of other property values of the multi-column element, such as [**column-width**](/css/properties/column-width).

## Examples

This example shows how to render text within the section.newspaper element in three columns.

``` css
#columns {
  -moz-column-count: 3; /* Firefox */
  -webkit-column-count: 3; /* Safari and Chrome */
  column-count: 3;
}
```

[View live example](http://code.webplatform.org/gist/6288917)

Using auto for column-count will allow as many columns as are necessary or able to be generated.

``` css
/* auto column-count allows n-columns of column-width */
div {
column-count: auto;
column-width: 100px;
}
```

## Notes

### Remarks

The actual column count may vary from the value specified due to available space. To ensure the specified value is used, all length property values of the multi-column element must be specified.

### Syntax

`column-count: count | auto`

## Related specifications

[CSS Multi-column Layout Module](http://www.w3.org/TR/css3-multicol/)
:   W3C Candidate Recommendation

## See also

### Related articles

#### Multi-Column

-   [break-after](/css/properties/break-after)

-   [break-before](/css/properties/break-before)

-   [break-inside](/css/properties/break-inside)

-   **column-count**

-   [column-gap](/css/properties/column-gap)

-   [column-rule](/css/properties/column-rule)

-   [column-rule-color](/css/properties/column-rule-color)

-   [column-rule-style](/css/properties/column-rule-style)

-   [column-rule-width](/css/properties/column-rule-width)

-   [column-span](/css/properties/column-span)

-   [column-width](/css/properties/column-width)

-   [content](/css/properties/content)

#### Responsive Web Design

-   [break-before](/css/properties/break-before)

-   **column-count**

-   [JavaScript animation](/tutorials/animation_in_javascript_2)

### Related pages

-   CSSStyleDeclaration[CSSStyleDeclaration](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)
-   currentStyle[currentStyle](/css/cssom/currentStyle)
-   style[style](/css/cssom/style)
-   table[table](/html/elements/table)
