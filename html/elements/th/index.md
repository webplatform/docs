---
title: 'th'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: th
  topic: html
notes:
  - 'Add description/notes, compatibility.'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLTableHeaderCellElement](/dom/HTMLTableHeaderCellElement)'
readiness: 'Not Ready'
summary: 'The th tag defines a header cell in an HTML table.'
tags:
  - Markup
  - Elements
  - HTML
uri: html/elements/th

---
## Summary

The th tag defines a header cell in an HTML table.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLTableHeaderCellElement](/dom/HTMLTableHeaderCellElement)

## Attributes

-   `colspan` = valid non-negative integer
    This attribute gives the number of columns respectively that the cell is to span.
-   `rowspan` = valid non-negative integer
    This attribute gives the number of rows respectively that the cell is to span. [[Example B]](#Example_B)
-   `headers` = unordered set of unique space-separated tokens
    The value of this attribute must have the value of an id attribute of the th element that is targeted. [[Example C]](#Example_C)
-   `scope` = row/ col/ rowgroup/ colgroup
    The scope attribute specifies the cell which the influence of headding cell reaches. [[Example D]](#Example_D)
    -   row
        The header cell applies to some of the subsequent cells in the same row(s).
    -   col
        The header cell applies to some of the subsequent cells in the same column(s).
    -   rowgroup
        The header cell applies to all the remaining cells in the row group. A th element's scope attribute must not be in the row group state if the element is not anchored in a row group.
    -   colgroup
        The header cell applies to all the remaining cells in the column group. A th element's scope attribute must not be in the column group state if the element is not anchored in a column group.

## Examples

This example uses the [**table**](/html/elements/table), [**td**](/html/elements/td), [**th**](/html/elements/thead), and [**tr**](/html/elements/tr).

``` html
<table>
    <tr>
      <th>
        This text is in the th
      </th>
    </tr>
    <tr>
      <td>
        This text is in the tbody.
      </td>
    </tr>
</table>
```

A table cell referring to the table header

``` html
<table>
  <caption>
    <p>table 1. List of HTML elements</p>
  </caption>
  <thead>
    <tr>
      <th id="c1">Number</th>
      <th id="c2">element</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td headers="c1">4.1.1</td>
      <td headers="c2">html</td>
    </tr>
    <tr>
      <td headers="c1">4.2.1</td>
      <td headers="c2">head</td>
    </tr>
  </tbody>
</table>
```

``` html
<table>
  <caption>
    <p>table 1. List of HTML elements</p>
  </caption>
  <thead>
    <tr>
      <th scope="row">Number</th>
      <th scope="row">element</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>4.1.1</td>
      <td>html</td>
    </tr>
    <tr>
      <td>4.2.1</td>
      <td>head</td>
    </tr>
  </tbody>
</table>
```

## Related specifications

[HTML 5.1](http://www.w3.org/TR/html51/tabular-data.html#the-th-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/tabular-data.html#the-th-element)
:   W3C Recommendation

[HTML 4.01](http://www.w3.org/TR/html401/struct/tables.html#edef-TH)
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

-   [td](/html/elements/td)

-   [tfoot](/html/elements/tfoot)

-   **th**

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

-   [td](/html/elements/td)

-   [tfoot](/html/elements/tfoot)

-   **th**
