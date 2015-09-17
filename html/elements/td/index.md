---
title: 'td'
compatibility:
  feature: td
  topic: html
notes:
  - 'Add description/notes, compatibility.'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLTableDataCellElement](/dom/HTMLTableDataCellElement)'
readiness: 'Almost Ready'
standardization_status: 'W3C Recommendation'
summary: 'Defines a standard Cell in an HTML table.'
tags:
  - Markup_Elements
  - HTML
uri: html/elements/td

---
## Summary

Defines a standard Cell in an HTML table.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLTableDataCellElement](/dom/HTMLTableDataCellElement)

## Attributes

-   `colspan` = valid non-negative integer
    This attribute gives the number of columns respectively that the cell is to span.
-   `rowspan` = valid non-negative integer
    This attribute gives the number of rows respectively that the cell is to span.
-   `headers` = unordered set of unique space-separated tokens
    The value of this attribute must have the value of an id attribute of the th element that is targeted.

## Examples

This example uses the [**table**](/html/elements/table) element with [**tr**](/html/elements/tr) and ****td**** to create a table with three rows and two columns.

``` html
<table border="1" width="80%">
  <tbody>
    <tr>
      <td>Row 1, Column 1 text.</td>
      <td>Row 1, Column 2 text.</td>
    </tr>
    <tr>
      <td>Row 2, Column 1 text.</td>
      <td>Row 2, Column 2 text.</td>
    </tr>
  </tbody>
</table>
```

## Related specifications

[HTML 5.1](http://www.w3.org/TR/html51/tabular-data.html#the-td-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/tabular-data.html#the-td-element)
:   W3C Recommendation

[HTML 4.01](http://www.w3.org/TR/html401/struct/tables.html#edef-TD)
:   W3C Recommendation

## See also

### Related articles

#### HTML

-   [user-modify](/css/properties/user-modify)

-   [textLength](/dom/HTMLTextAreaElement/textLength)

-   [value](/dom/HTMLTextAreaElement/value)

-   [accept](/html/attributes/accept)

-   [action](/html/attributes/action)

-   [alt](/html/attributes/alt)

-   [autocomplete](/html/attributes/autocomplete)

-   [autofocus](/html/attributes/autofocus)

-   [checked](/html/attributes/checked)

-   [crossorigin](/html/attributes/crossorigin)

-   [form](/html/attributes/form)

-   [formEnctype](/html/attributes/formEnctype)

-   [height](/html/attributes/height)

-   [list](/html/attributes/list)

-   [max (HTMLInputElement)](/html/attributes/max_(HTMLInputElement))

-   [maxLength](/html/attributes/maxLength)

-   [min](/html/attributes/min)

-   [multiple](/html/attributes/multiple)

-   [readonly](/html/attributes/readonly)

-   [size](/html/attributes/size)

-   [standby](/html/attributes/standby)

-   [step](/html/attributes/step)

-   [HTML Elements](/html/elements)

-   [!DOCTYPE](/html/elements/!DOCTYPE)

-   [!DOCTYPE](/html/elements/!DOCTYPE/ja)

-   [acronym](/html/elements/acronym)

-   [b](/html/elements/b)

-   [b](/html/elements/b/ja)

-   [br](/html/elements/br)

-   [br](/html/elements/br/ja)

-   [button](/html/elements/button)

-   [button](/html/elements/button/ja)

-   [caption](/html/elements/caption)

-   [cite](/html/elements/cite)

-   [code](/html/elements/code)

-   [col](/html/elements/col)

-   [colgroup](/html/elements/colgroup)

-   [datalist](/html/elements/datalist)

-   [del](/html/elements/del)

-   [dfn](/html/elements/dfn)

-   [div](/html/elements/div)

-   [em](/html/elements/em)

-   [EMBED](/html/elements/embed)

-   [fieldset](/html/elements/fieldset)

-   [font](/html/elements/font)

-   [footer](/html/elements/footer)

-   [head](/html/elements/head)

-   [hn](/html/elements/hn)

-   [hr](/html/elements/hr)

-   [html](/html/elements/html)

-   [i](/html/elements/i)

-   [img](/html/elements/img)

-   [input](/html/elements/input)

-   [ins](/html/elements/ins)

-   [kbd](/html/elements/kbd)

-   [legend](/html/elements/legend)

-   [mark](/html/elements/mark)

-   [option](/html/elements/option)

-   [p](/html/elements/p)

-   [samp](/html/elements/samp)

-   [script](/html/elements/script)

-   [span](/html/elements/span)

-   [strong](/html/elements/strong)

-   [table](/html/elements/table)

-   [tbody](/html/elements/tbody)

-   **td**

-   [tfoot](/html/elements/tfoot)

-   [th](/html/elements/th)

-   [time](/html/elements/time)

#### Tables

-   [border-collapse](/css/properties/border-collapse)

-   [border-spacing](/css/properties/border-spacing)

-   [caption-side](/css/properties/caption-side)

-   [empty-cells](/css/properties/empty-cells)

-   [Tables](/css/tables)

-   [col](/html/elements/col)

-   [colgroup](/html/elements/colgroup)

-   [table](/html/elements/table)

-   [tbody](/html/elements/tbody)

-   **td**

-   [tfoot](/html/elements/tfoot)

-   [th](/html/elements/th)
