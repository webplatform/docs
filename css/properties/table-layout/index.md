---
title: table layout
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/7044174'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`auto`'
  'Applies to': 'Table and inline-table elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'As specified'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`object.style.tableLayout`'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'The ''table-layout'' property controls the algorithm used to lay out the table cells, rows, and columns.'
tags:
  - CSS
  - Properties
uri: css/properties/table-layout

---
## <span>Summary</span>

The 'table-layout' property controls the algorithm used to lay out the table cells, rows, and columns.

## <span>Overview table</span>

[Initial value](/css/concepts/initial_value)
:   `auto`

Applies to
:   Table and inline-table elements

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   As specified

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `object.style.tableLayout`

## <span>Syntax</span>

-   `table-layout: auto`
-   `table-layout: fixed`
-   `table-layout: inherit`

## <span>Values</span>

auto
:   Default. Column width is set by the widest unbreakable content in the column cells. The width of the table and its cells depends on the content of the cells.

fixed
:   Table and column widths are set by the widths of table and col elements or by the width of the first row of cells. It does not depend on the content of the cells. Rendering is faster as the user agent can begin to lay out the table once the entire first row has been received. Cells in subsequent rows do not affect column widths.

inherit
:   This features inherits table-layout property from the parent element.

## <span>Examples</span>

This example shows table-layout 'auto' and 'fixed'. With 'auto', the column stretches to encompass the largest unbreakable element. With 'fixed', the column gets the defined width, even though the content might not fit.

``` html
<p><strong>table-layout: auto</strong></p>
<table border="1">
    <tr>
        <td class="first"><p>cell 1, Lorem ipsum</p></td>
        <td><p>cell 2</p></td>
    </tr>
    <tr>
        <td><p>cell 3, Suspendisse in elit lectus.</p></td>
        <td><p>cell 4</p></td>
    </tr>
</table>

<p><strong>table-layout: fixed</strong></p>
<table border="1" class="fixed">
    <tr>
        <td class="first"><p>cell 1, Lorem ipsum</p></td>
        <td><p>cell 2</p></td>
    </tr>
    <tr>
        <td><p>cell 3, Suspendisse in elit lectus.</p></td>
        <td><p>cell 4</p></td>
    </tr>
</table>

<p><strong>table-layout: fixed with overflow set to hidden</strong></p>
<table border="1" class="fixed2">
    <tr>
        <td class="first"><p>cell 1, Lorem ipsum</p></td>
        <td><p>cell 2</p></td>
    </tr>
    <tr>
        <td><p>cell 3, Suspendisse in elit lectus.</p></td>
        <td><p>cell 4</p></td>
    </tr>
</table>
```

[View live example](http://code.webplatform.org/gist/7044174)

Here's the CSS for styling the table, above.

``` css
/**
 * Table-layout - Web Platform Docs Examples
 *
 * An example of table-layout 'auto' and 'fixed'
 * With 'auto', the column stretches to encompass the largest unbreakable element
 * With 'fixed', the column gets the defined width, even though the content might not fit
 *
 * @author  Vivienne van Velzen
 * @see     http://docs.webplatform.org/wiki/css/properties/table-layout
 */

table {
    border-color: #F00;
    width: 400px;
    table-layout: auto; /* default */
}
table.fixed,
table.fixed2 {
    table-layout: fixed;
}
td {
    border-color: #00F;
}
td.first {
    width: 50px;
}
table.fixed2 td {
    overflow: hidden;
}
p {
    margin: 15px 0 3px 0;
}
td p {
    margin: 3px;
}
```

[View live example](http://code.webplatform.org/gist/7044174)

## <span>Notes</span>

-   When using 'table-layout: fixed', authors should not omit columns from the first row. If a subsequent row has more columns than the greater of the number determined by the table-column elements and the number determined by the first row, then additional columns may not be rendered.
-   If 'table-layout: fixed', any cell that has content that overflows uses the overflow property to determine whether to clip the overflow content.

## <span>Related specifications</span>

[CSS2.1, 17.5.2 Table width algorithms: the 'table-layout' property](http://www.w3.org/TR/CSS2/tables.html#width-layout)
:   W3C Recommendation
