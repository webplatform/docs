---
title: 'col'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: col
  topic: html
notes:
  - 'Add Category, Parent, Children and Compatibility information. Modify DOM Interface information.'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLTableColElement](/dom/HTMLTableColElement)'
readiness: 'In Progress'
summary: 'The col element (&lt;col&gt;) specifies  properties for each column within a &lt;colgroup&gt; element in a &lt;table&gt;.'
tags:
  - Markup_Elements
  - HTML
uri: html/elements/col

---
## Summary

The col element (&lt;col&gt;) specifies properties for each column within a &lt;colgroup&gt; element in a &lt;table&gt;.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLTableColElement](/dom/HTMLTableColElement)

## Examples

This example uses the **col** element to specify characteristics for default columns in a table.

``` html
<HTML>
<BODY>
<TABLE BORDER="2" RULES="groups">
<!-- RULES is set to "groups", which has no effect in this sample. For this
attribute to work, you must use COLSPAN to define the groups of columns.-->
    <COL SPAN="2" STYLE="color:red">
    <COL STYLE="color:blue">
    <TR>
        <TD>This column is in the first group.</TD>
        <TD>This column is in the first group.</TD>
        <TD>This column is in the second group.</TD>
    </TR>
    <TR>
        <TD>This column is in the first group.</TD>
        <TD>This column is in the first group.</TD>
        <TD>This column is in the second group.</TD>
    </TR>
</TABLE>
</BODY>
</HTML>
```

## Notes

### Remarks

**COL** elements can be nested within a **COLGROUP** element. If this is done, the nested **COL** attributes override the **COLGROUP** attributes. You can use the **COL** and **COLGROUP** elements for similar purposes. However, you must use the **COLGROUP** element to determine where table internal dividing lines ([**rules**](/html/attributes/rules)) should go. This is illustrated in the following example. Use the [**SPAN**](/html/attributes/span) attribute to specify the number of table columns that the **COLGROUP** defines. This attribute has a default value equal to one. The [**table**](/html/elements/table) object and its associated elements have a separate table object model, which uses different methods than the general object model. For more information on the table object model, see Building Tables Dynamically.

## Related specifications

[HTML 5.1](http://www.w3.org/TR/html51/tabular-data.html#the-col-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/tabular-data.html#the-col-element)
:   W3C Recommendation

[HTML 4.01](http://www.w3.org/TR/html401/struct/tables.html#edef-COL)
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

-   **col**

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

-   [th](/html/elements/th)

-   [time](/html/elements/time)

#### Tables

-   [border-collapse](/css/properties/border-collapse)

-   [border-spacing](/css/properties/border-spacing)

-   [caption-side](/css/properties/caption-side)

-   [empty-cells](/css/properties/empty-cells)

-   [Tables](/css/tables)

-   **col**

-   [colgroup](/html/elements/colgroup)

-   [table](/html/elements/table)

-   [tbody](/html/elements/tbody)

-   [td](/html/elements/td)

-   [tfoot](/html/elements/tfoot)

-   [th](/html/elements/th)

### Other articles

-   [colgroup](/html/elements/colgroup)
