---
title: 'widows'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: widows
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`2`'
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'Yes'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'As specified'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
  Percentages: N/A
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: "Defines the minimum number of lines that can appear in the beginning of a new page. In typography, a widow is the last line of a paragraph appearing alone at the top of a page, which is considered to look awkward. Setting the widows property to an integer higher than 1 prevents this.\n"
tags:
  - CSS_Properties
  - CSS
uri: css/properties/widows

---
## Summary

Defines the minimum number of lines that can appear in the beginning of a new page. In typography, a widow is the last line of a paragraph appearing alone at the top of a page, which is considered to look awkward. Setting the widows property to an integer higher than 1 prevents this.

On a non-paged media, like screen, the widows CSS property has no effect. It can have a number value or it can inherit the values from the parent element.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `2`

Applies to
:   All elements

[Inherited](/css/concepts/inherited)
:   Yes

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   As specified

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:

Percentages
:   N/A

## Syntax

-   `widows: inherit`
-   `widows: integer`

## Values

integer
:   Denotes the minimum number of lines that can appear alone on the top of a new page. If the value is not positive, the declaration is invalid.

inherit
:   Takes the same specified value as the property for the element's parent.

## Examples

The following style rule ensures that at least three lines of a paragraph appear at the top (*widows*) and bottom (*orphans*) of each printed page.

``` css
@media print {
    p {
        widows: 3;
        orphans: 3;
    }
}
```

## Notes

### Remarks

The **widows** property takes precedence over [**orphans**](/css/properties/orphans).

## Related specifications

[CSS Fragmentation Module Level 3](http://www.w3.org/TR/css3-break/#widows-orphans)
:   W3C Working Draft

[CSS Multi-column Layout Module](http://dev.w3.org/csswg/css-multicol/#filling-columns)
:   W3C Candidate Reccomendation

[CSS Level 2 (Revision 1)](http://www.w3.org/TR/CSS2/page.html#break-inside)
:   W3C Recommendation

## See also

### Related articles

#### Paged Media

-   [@page](/css/atrules/@page)

-   **widows**

### External resources

<http://xhtml.com/en/css/reference/widows/>

### Related pages

-   orphans[orphans](/css/properties/orphans)
-   CSSStyleDeclaration[CSSStyleDeclaration](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)
-   currentStyle[currentStyle](/css/cssom/currentStyle)
-   runtimeStyle[runtimeStyle](/css/cssom/runtimeStyle)
-   style[style](/css/cssom/style)
