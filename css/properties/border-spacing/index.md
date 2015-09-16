---
title: border-spacing
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/6948537'
notes:
  - 'Add example, compatibility.'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`0`'
  'Applies to': 'Table and inline-table elements'
  '[Inherited](/css/concepts/inherited)': 'Yes'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'Two absolute lengths'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`borderSpacing`'
readiness: 'In Progress'
standardization_status: 'W3C Recommendation'
summary: 'Specifies the distance between the borders of adjacent cells.'
tags:
  - CSS
  - Properties
uri: css/properties/border-spacing

---
## Summary

Specifies the distance between the borders of adjacent cells.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `0`

Applies to
:   Table and inline-table elements

[Inherited](/css/concepts/inherited)
:   Yes

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   Two absolute lengths

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `borderSpacing`

## Syntax

-   `border-spacing: inherit`
-   `border-spacing: length`

## Values

length
:   The distance that separates adjoining cell borders. If one length is specified, it gives both the horizontal and vertical spacing. If two are specified, the first gives the horizontal spacing and the second the vertical spacing. Lengths may not be negative.

inherit
:   The same specified value as the property for the element's parent will be used.

## Examples

``` html

```

[View live example](http://code.webplatform.org/gist/6948537)

## Notes

-   The CSS2.1 specification states that user agents may apply this property to frameset elements (therefore replacing the framespacing attribute).

## Related specifications

[CSS 2.1, 17.6.1. The separated borders model](http://www.w3.org/TR/CSS2/tables.html#propdef-border-spacing)
:   Recommendation

[CSS 3, 8.1. The separated borders model](http://dev.w3.org/csswg/css3-tables/#border-spacing)
:   Editor's Draft

## See also

### Related articles

#### Tables

-   [border-collapse](/css/properties/border-collapse)

-   **border-spacing**

-   [caption-side](/css/properties/caption-side)

-   [empty-cells](/css/properties/empty-cells)

-   [Tables](/css/tables)

-   [col](/html/elements/col)

-   [colgroup](/html/elements/colgroup)

-   [table](/html/elements/table)

-   [tbody](/html/elements/tbody)

-   [td](/html/elements/td)

-   [tfoot](/html/elements/tfoot)

-   [th](/html/elements/th)
