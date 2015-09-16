---
title: 'orphans'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: orphans
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`2`'
  'Applies to': 'Block containers'
  '[Inherited](/css/concepts/inherited)': 'Yes'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'As specified'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`orphans`'
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: "In typography terms, an orphan is the first line of a paragraph that is left behind on the old page while the paragraph continues on the next. The orphans CSS property refers to the minimum number of lines in a block container that must be left at the bottom of the old page. This property is normally used to control how page breaks occur. This property only affects paged media such as print.\nFor example, if a paragraph can't fit on one page in its entirety it is split wherever it is possible. In this way single lines of a paragraph can appear on page before it continues on the next page. This is usually unwanted, so many word processors require at least two lines to be left on an old page, instead of one. You can give it either a positive number (where 2 is the default) or inherit.\n"
tags:
  - CSS
  - Properties
uri: css/properties/orphans

---
## Summary

In typography terms, an orphan is the first line of a paragraph that is left behind on the old page while the paragraph continues on the next. The orphans CSS property refers to the minimum number of lines in a block container that must be left at the bottom of the old page. This property is normally used to control how page breaks occur. This property only affects paged media such as print. For example, if a paragraph can't fit on one page in its entirety it is split wherever it is possible. In this way single lines of a paragraph can appear on page before it continues on the next page. This is usually unwanted, so many word processors require at least two lines to be left on an old page, instead of one. You can give it either a positive number (where 2 is the default) or inherit.

Note that the orphan property does not generally affect non-paged media such as screen. However, browsers supporting both orphans and columns will apply the intended functionality to columns as well. Also, the property only affects block-level elements.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `2`

Applies to
:   Block containers

[Inherited](/css/concepts/inherited)
:   Yes

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   As specified

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `orphans`

## Syntax

-   `orphans: inherit`
-   `orphans: integer`

## Values

integer
:   Only positive values are allowed.

An **Integer** that specifies or receives the minimum number of lines to print at the bottom of a page.

inherit
:   Takes the same specified value as the property for the element's parent.

## Examples

The following style rule ensures that at least three lines of a paragraph appear at the bottom and top of each printed page.

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

The [**widows**](/css/properties/widows) property takes precedence over **orphans**.

## Related specifications

[CSS Fragmentation Module Level 3](http://www.w3.org/TR/css3-break/#widows-orphans)
:   W3C Working Draft

[CSS Paged Media Module Level 3](http://dev.w3.org/csswg/css-page/#orphans)
:   W3C Editor's Draft

[CSS Level 2 (Revision 1)](http://www.w3.org/TR/CSS2/page.html#propdef-orphans)
:   W3C Reccomendation

## See also

### Related pages

-   widows[widows](/css/properties/widows)
-   CSSStyleDeclaration[CSSStyleDeclaration](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)
-   currentStyle[currentStyle](/css/cssom/currentStyle)
-   runtimeStyle[runtimeStyle](/css/cssom/runtimeStyle)
-   style[style](/css/cssom/style)
