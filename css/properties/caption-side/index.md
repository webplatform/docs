---
title: caption-side
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Complete specifications, compatibility.'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`top`'
  'Applies to': 'Table-caption elements'
  '[Inherited](/css/concepts/inherited)': 'Yes'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': ''
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
readiness: 'In Progress'
summary: 'Specifies the placement of a table caption.'
tags:
  - CSS
  - Properties
uri: css/properties/caption-side

---
## Summary

Specifies the placement of a table caption.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `top`

Applies to
:   Table-caption elements

[Inherited](/css/concepts/inherited)
:   Yes

Media
:   visual

[Computed value](/css/concepts/computed_value)
:

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:

## Syntax

-   `caption-side: bottom`
-   `caption-side: inherit`
-   `caption-side: top`

## Values

top
:   Positions the caption box above the table box.

bottom
:   Positions the caption box below the table box.

inherit
:   Takes the same specified value as the property for the element's parent.

## Examples

The following example constructs a table with standard HTML elements. The style rule places the caption above the table.

``` html
<meta http-equiv="X-UA-Compatible" content="IE=8" />

<style type="text/css">
caption {
    caption-side:top;
}
</style>
<table><tr><td>A simple table.</td></tr>
<caption>Table caption.</caption>
</table>
```

This example uses CSS to construct a table using [**display**](/css/properties/display) attributes. This caption is also placed above its associated table.

``` html
<meta http-equiv="X-UA-Compatible" content="IE=8" />

<style type="text/css">
.table {
    display:table;
    border:1px #eee outset;
    border-spacing:2px;
}
.cell {
    display:table-cell;
    border:1px solid black;
}
.caption {
    display:table-caption;
    caption-side:top;
}
</style>
<div class="table">
<span class="cell">Table content.</span>
<em class="caption">A caption.</em>
</div>
```

## Notes

### Remarks

The supported possible values for **caption-side** depend on the orientation of the table. Horizontal tables support the top and bottom values. Vertical tables support the left and right values. Using an unsupported value for this property (for instance, `left` on a caption for a horizontal table) will cause the caption to appear at the "logical top" of the table. The logical top of a table depends on the writing mode of the text, and is parallel to and immediately precedes the first line of text in a table. Captions placed to the left or right of the table are not rotated so as to be read vertically. This style attribute can be applied to any element with a [**display**](/css/properties/display) style of **table-caption**.

### Syntax

`caption-side: top | bottom`

### Standards information

-   [CSS 2.1](http://go.microsoft.com/fwlink/p/?linkid=203757), Section 17.4.1

## See also

### Related articles

#### Tables

-   [border-collapse](/css/properties/border-collapse)

-   [border-spacing](/css/properties/border-spacing)

-   **caption-side**

-   [empty-cells](/css/properties/empty-cells)

-   [Tables](/css/tables)

-   [col](/html/elements/col)

-   [colgroup](/html/elements/colgroup)

-   [table](/html/elements/table)

-   [tbody](/html/elements/tbody)

-   [td](/html/elements/td)

-   [tfoot](/html/elements/tfoot)

-   [th](/html/elements/th)

### Related pages

-   `CSSStyleDeclaration`
-   `currentStyle`
-   `runtimeStyle`
-   `style`
-   `display`
