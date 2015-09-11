---
title: table
notes:
  - 'Add description, notes, compatibility.'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLTableElement](/dom/HTMLTableElement)'
readiness: 'Not Ready'
standardization_status: 'W3C Recommendation'
summary: 'The &lt;table&gt; element is a wrapper for an HTML table. It defines the start and end of a table, and can contain other table elements, such as &lt;tr&gt;.'
tags:
  - Markup
  - Elements
  - HTML
uri: html/elements/table

---
## <span>Summary</span>

The &lt;table&gt; element is a wrapper for an HTML table. It defines the start and end of a table, and can contain other table elements, such as &lt;tr&gt;.

## <span>Overview Table</span>

[DOM Interface](/dom/interface)
:   [HTMLTableElement](/dom/HTMLTableElement)

The `<table>` element is a container for HTML table data, which is used to mark up tabular data. Tabular data is any data that can be systematically displayed in rows and columns, for example, "See table 3 for an example."

Tables were often used for laying out web pages because tables helped fix the position of text on the page, however, this use has become an outdated. We recommend you use `<div>` and `<span>` for fixed layouts. You can still use tables for tabular data.

You might find working with an HTML table editor easier than coding tables by hand, unless you are especially adept at visualizing table row and columns using the appropriate HTML tags. It is easy to miss or drop a tag when coding tables manually, which will cause your table to be malformed.

## <span>Examples</span>

This example uses the [**tbody**](/html/elements/tbody) element with the ****table****, [**td**](/html/elements/td), [**thead**](/html/elements/thead), and [**tr**](/html/elements/tr) elements to create a table with the first row in the table head and the second row in the table body.

``` html
<table>
  <thead>
    <tr>
      <td>
        This text is in the thead.
      </td>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        This text is in the tbody.
      </td>
    </tr>
  </tbody>
</table>
```

## <span>Usage</span>

     At the most simple level you need to use the following three groups of tags to create a basic table.

1)

<table>
</table>
<table>
tag begins the table, and \<ltable\> tag ends the table. 2\> \<tr\</tr\>

<tr>
creates a row while

</tr>
ends the row. 3\>

<td>
</td>
<td>
creates a column space while

</td>
ends the column space. These are usually nested inside a pair of

<tr>
</tr>
tags. The term "td" stands for table data, but as a representation, you can view it like a "column tag".

The three pairs of tags can create a simple two row, two column table using the code below.

||
|row 1 col 1|row 1 col 2|
|row 1 col 2|row 2 col 2|

## <span>Related specifications</span>

[HTML 5.1](http://www.w3.org/TR/html51/tabular-data.html#the-table-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/tabular-data.html#the-table-element)
:   W3C Recommendation

[HTML 4.01](http://www.w3.org/TR/html401/struct/tables.html#edef-TABLE)
:   W3C Recommendation

## <span>See also</span>

### <span>Related articles</span>

#### <span>HTML</span>

-   [user-modify](/css/properties/user-modify)

-   [HTMLAudioElement](/dom/HTMLAudioElement)

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

-   **table**

-   [tbody](/html/elements/tbody)

-   [td](/html/elements/td)

-   [tfoot](/html/elements/tfoot)

-   [th](/html/elements/th)

-   [time](/html/elements/time)

#### <span>Tables</span>

-   [border-collapse](/css/properties/border-collapse)

-   [border-spacing](/css/properties/border-spacing)

-   [caption-side](/css/properties/caption-side)

-   [empty-cells](/css/properties/empty-cells)

-   [Tables](/css/tables)

-   [col](/html/elements/col)

-   [colgroup](/html/elements/colgroup)

-   **table**

-   [tbody](/html/elements/tbody)

-   [td](/html/elements/td)

-   [tfoot](/html/elements/tfoot)

-   [th](/html/elements/th)

</table>
