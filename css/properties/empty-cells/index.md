---
title: empty-cells
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/5842874'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`show`'
  'Applies to': 'table-cell elements'
  '[Inherited](/css/concepts/inherited)': 'Yes'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'Same as specified'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`emptyCells`'
readiness: 'Ready to Use'
summary: 'Sets whether or not to display borders and background on empty cells in a table.'
tags:
  - CSS
  - Properties
uri: css/properties/empty-cells

---
## <span>Summary</span>

Sets whether or not to display borders and background on empty cells in a table.

## <span>Overview table</span>

[Initial value](/css/concepts/initial_value)
:   `show`

Applies to
:   table-cell elements

[Inherited](/css/concepts/inherited)
:   Yes

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   Same as specified

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `emptyCells`

## <span>Syntax</span>

-   `empty-cells: hide`
-   `empty-cells: show`

## <span>Values</span>

show
:   Renders empty cells with inherited borders and styles

hide
:   Does not render the cell

## <span>Examples</span>

``` css
/*
  * This example hides any table cell that has no data in it
  */

td{
    empty-cells: hide;
}
```

[View live example](http://code.webplatform.org/gist/5842874)

## <span>Notes</span>

### <span>Remarks</span>

If all cells in a particular row have the **empty-cells** value set to **hide**, the entire row will behave as if it had the [**display**](/css/properties/display) value of `none`. The **empty-cells** value can be set for an entire table. If the value is set in the [**table**](/html/elements/table) properties to `show`,all cells will be rendered with borders, regardless of their content.

### <span>Syntax</span>

`empty-cells: show | hide`

### <span>Standards information</span>

-   [CSS 2.1](http://go.microsoft.com/fwlink/p/?linkid=203757), Section 17.6.1.1

## <span>See also</span>

### <span>Related articles</span>

#### <span>Tables</span>

-   [border-collapse](/css/properties/border-collapse)

-   [border-spacing](/css/properties/border-spacing)

-   [caption-side](/css/properties/caption-side)

-   **empty-cells**

-   [Tables](/css/tables)

-   [col](/html/elements/col)

-   [colgroup](/html/elements/colgroup)

-   [table](/html/elements/table)

-   [tbody](/html/elements/tbody)

-   [td](/html/elements/td)

-   [tfoot](/html/elements/tfoot)

-   [th](/html/elements/th)

### <span>Related pages (MSDN)</span>

-   `CSSStyleDeclaration`
-   `currentStyle`
-   `runtimeStyle`
-   `style`
