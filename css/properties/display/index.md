---
title: 'display'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
compatibility:
  feature: display
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`inline`'
  'Applies to': 'All elements.'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'See individual properties.'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
  Percentages: 'See individual properties.'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'This property specifies the type of rendering box used for an element. It is a shorthand property for many other display properties.'
tags:
  - CSS_Properties
  - CSS
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - css/properties/af
    - css/properties/ar
    - css/properties/ast
    - css/properties/az
    - css/properties/bcc
    - css/properties/bg
    - css/properties/br
    - css/properties/ca
    - css/properties/cs
    - css/properties/da
    - css/properties/de
    - css/properties/diq
    - css/properties/el
    - css/properties/eo
    - css/properties/es
    - css/properties/fa
    - css/properties/fi
    - css/properties/fr
    - css/properties/gl
    - css/properties/gu
    - css/properties/he
    - css/properties/hu
    - css/properties/hy
    - css/properties/id
    - css/properties/it
    - css/properties/ja
    - css/properties/ka
    - css/properties/kk
    - css/properties/km
    - css/properties/ko
    - css/properties/ksh
    - css/properties/kw
    - css/properties/mk
    - css/properties/ml
    - css/properties/mr
    - css/properties/ms
    - css/properties/nl
    - css/properties/no
    - css/properties/oc
    - css/properties/pl
    - css/properties/pt
    - css/properties/pt-br
    - css/properties/ro
    - css/properties/ru
    - css/properties/si
    - css/properties/sk
    - css/properties/sl
    - css/properties/sq
    - css/properties/sr
    - css/properties/sv
    - css/properties/ta
    - css/properties/th
    - css/properties/tr
    - css/properties/uk
    - css/properties/vi
    - css/properties/yue
    - css/properties/zh
    - css/properties/zh-hans
    - css/properties/zh-hant
    - css/properties/zh-tw
uri: css/properties/display

---
## Summary

This property specifies the type of rendering box used for an element. It is a shorthand property for many other display properties.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `inline`

Applies to
:   All elements.

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   See individual properties.

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:

Percentages
:   See individual properties.

## Syntax

-   `display: block`
-   `display: flex`
-   `display: grid`
-   `display: inherit`
-   `display: inline`
-   `display: inline-block`
-   `display: inline-flex`
-   `display: inline-grid`
-   `display: inline-list-item`
-   `display: list-item`
-   `display: none`
-   `display: table, inline-table, table-row-group, table-column, table-column-group, table-header-group, table-footer-group, table-row, table-cell, table-caption`

## Values

inline
:   Generates one or more inline element boxes.

block
:   Generates a block element box.

list-item
:   Generates a principal block box and a marker box.

inline-list-item
:   Generates an inline principal block box and a marker box.

inline-block
:   Generates a block element box that flows with surrounding content as if it were a single inline box--and behaves like a replaced element.

flex
:   Generates a block element for laying out content in the flexbox model. This is a flexbox model value in CSS3. See [flex](/css/properties/flex).

inline-flex
:   Generates an inline element for laying out content in the flexbox model. This is a flexbox model value in CSS3. See [flex](/css/properties/flex).

grid
:   Generates a block element for laying out content in the grid model. This is a grid box model value (an experimental tag in CSS 3.0). See [grid](/css/properties/grid).

inline-grid
:   Generates an inline element for laying out content in the grid model. This is a grid box model value (an experimental tag in CSS 3.0). See [grid](/css/properties/grid).

none
:   Causes an element to not appear in the formatting structure and have no effect on layout. Descendant elements and their content are likewise removed from the formatting structure. (This behavior cannot be overridden by setting the *display* property on the descendants.) **Note:** A display value of "none" does not create an invisible box; it creates no box at all. To render an element box's dimensions, yet have its contents be invisible, use the *visibility* property; see [visibility](/css/properties/visibility).

inherit
:   Causes an element to use the specified or computed value of that property on its parent element.

table, inline-table, table-row-group, table-column, table-column-group, table-header-group, table-footer-group, table-row, table-cell, table-caption
:   These values cause an element to behave like a table element, subject to certain restrictions. See the [W3C tables specification](http://www.w3.org/TR/CSS2/tables.html).

## Examples

Change a `span` element from its initial display `inline` to display as block-level element.

``` html
Some example text
<style>
  span {
    display: block;
  }
</style>
```

Do not display an element by using `display: none;`.

``` html
<div>Some example text</div>
<style>
  div {
    display: none;
  }
</style>
```

Specify the rendering type as block or inline to define how the element will display. Set the element to inherit the rendering values of its parent container:

``` css
p.block {
    /* Sets the element to display in a box model rendering type. */
    display:block;
}

p.inline {
    /* Sets the element to display inline inside the current element. */
    display:inline;
}

p.inherit {
    /* Sets the display value to inherit its parent container's display values. */
    display:inherit;
}
```

Mobile-adapt a table, suppressing column headers and re-inserting text next to vertically stacked cells:

``` css
@media (max-width:400px) {
    /* stack cells vertically... */
    table, tr, td, th, tbody { display: block }
    /* ...but hide column headers */
    thead { display: none }
    /* insert column header text next to content */
    td::before { font-weight: bold }
    td:nth-of-type(1)::before { content: "Column 1: " }
    td:nth-of-type(2)::before { content: "Column 2: " }
    td:nth-of-type(3)::before { content: "Column 3: " }
    td:nth-of-type(4)::before { content: "Column 4: " }
}
```

Stack generously sized links in mobile interface to extend the touch zone to the full width of the screen:

``` css
@media (max-width:400px) {
    a[href] {
        display: block;
        padding: 12px;
        border-radius: 12px;
        margin: 6px;
        text-decoration: none;
        color: #000;
        background-color: #fff;
        background-image: url(/img/nav_icon.png);
        background-position: 90% center;
    }
}
```

## Notes

**Computed value and relationship between **display**, [position](/css/properties/position), and [float](/css/properties/float)**

-   If 'display' has the value 'none', then 'position' and 'float' do not apply. In this case, the element generates no box.
-   Otherwise, if 'position' has the value 'absolute' or 'fixed', the box is absolutely positioned, the computed value of 'float' is 'none', and display is set according to the table below. The position of the box will be determined by the 'top', 'right', 'bottom' and 'left' properties and the box's containing block.
-   Otherwise, if 'float' has a value other than 'none', the box is floated and 'display' is set according to the table below.
-   Otherwise, if the element is the root element, 'display' is set according to the table below, except that it is undefined in CSS 2.1 whether a specified value of 'list-item' becomes a computed value of 'block' or 'list-item'.
-   Otherwise, the remaining 'display' property values apply as specified.

|Specified value|Computed value|
|:--------------|:-------------|
|inline-table|table|
|inline, run-in, table-row-group, table-column,
table-column-group, table-header-group,
 table-footer-group, table-row, table-cell,
table-caption, inline-block|block|
|others|same as specified|

**Table-designated elements**
 The Cascading Style Sheets (CSS) table display model does not require explicit elements to correspond with the HTML tags. For example, an element styled as `display: table-cell` does not need to be contained within a block that is styled `display: table-row` to be styled correctly. Implicit table elements are created as necessary in an attempt to make the document valid. Contrast this behavior to the traditional HTML table model, where table elements are implicitly closed early to avoid unexpected nesting.

## Related specifications

[CSS Display Module Level 3](http://dev.w3.org/csswg/css-display-3/)
:   Editor's Draft

[CSS Level 2 (Revision 1)](http://www.w3.org/TR/CSS2/visuren.html#display-prop)
:   Recommendation

