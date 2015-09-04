---
title: colgroup
tags:
  - Markup
  - Elements
  - HTML
readiness: 'In Progress'
standardization_status: 'W3C Recommendation'
notes:
  - 'Add Category, Parent, Children and Compatibility information.'
summary: "The colgroup element (<colgroup>) specifies a group of one or more columns in a table for formatting.\nThis element is useful for applying properties to entire columns, instead of repeating the properties for each cell, for each row.\n"
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/colgroupEX1.htm'
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/colgroupEX2.htm'
uri: html/elements/colgroup

---
# colgroup

## Summary

The colgroup element (\<colgroup\>) specifies a group of one or more columns in a table for formatting. This element is useful for applying properties to entire columns, instead of repeating the properties for each cell, for each row.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLTableColElement](/dom/HTMLTableColElement)

## HTML Attributes

-   `span` = valid non-negative integer

## Examples

This example uses the **COLGROUP** element to assign specific characteristics to two groups of columns in a table.

    <html>
    <body>
    <table border="2" rules="groups">
        <!-- RULES is set to "groups", which places internal dividing lines around
    table columns defined by COLGROUP. -->
        <colgroup span="2" style="color: red">
        </colgroup>
        <colgroup style="color: blue">
        </colgroup>
        <tr>
            <td>This column is in the first group.</td>
            <td>This column is in the first group.</td>
            <td>This column is in the second group.</td>
        </tr>
        <tr>
            <td>This column is in the first group.</td>
            <td>This column is in the first group.</td>
            <td>This column is in the second group.</td>
        </tr>
    </table>
    </body>
    </html>

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/colgroupEX1.htm)

When **COL** elements are nested inside a **COLGROUP** element, the attributes of the **COL** elements override the attributes of the **COLGROUP** element. In this example, the last column has no formatting even though **COLGROUP** spans over all three columns. This happens because the [**SPAN**](/html/attributes/span) attribute of the nested **COL** element overrides the **SPAN** attribute of the **COLGROUP**.

    <html>
    <body>
    <table border="2">
        <colgroup span="3" style="color: green; background: black">
            <!-- Styling is applied to only the first two columns, instead of all
        three, and the font color is red instead of green. This is consistent
        with the attributes of the COL element. -->
            <col span="2" style="color: red">
        </colgroup>
        <tr>
            <td>This column is in the first group.</td>
            <td>This column is in the first group.</td>
            <td>This column is in the second group.</td>
        </tr>
        <tr>
            <td>This column is in the first group.</td>
            <td>This column is in the first group.</td>
            <td>This column is in the second group.</td>
        </tr>
    </table>
    </body>
    </html>

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/colgroupEX2.htm)

## Notes

### Remarks

Nested **COL** elements override **COLGROUP** elements. Use the [**SPAN**](/html/attributes/span) attribute to specify the number of table columns that the **COLGROUP** defines. This attribute has a default value equal to one.

**COL** elements can occur outside of a **COLGROUP** element, and these two elements can be used for similar purposes. However, you must use the **COLGROUP** element to determine where table internal dividing lines ([**rules**](/html/attributes/rules)) should go. This is illustrated in the first example .

You should avoid using the [**SPAN**](/html/attributes/span) attribute inside the **COLGROUP** element if there are **COL** elements nested within it. This is because the **SPAN** attribute that belongs to the nested **COL** elements will override the attribute that belongs to the **COLGROUP** element. This can cause confusing code and possibly unintended results. This behavior is illustrated in the second example.

The [**table**](/html/elements/table) object and its associated elements have a separate table object model, which uses different methods than the general object model. For more information on the table object model, see Building Tables Dynamically.

## Related specifications

Specification
:   Status
[HTML 5.1](http://www.w3.org/TR/html51/tabular-data.html#the-colgroup-element)
:   W3C Working Draft
[HTML 5](http://www.w3.org/TR/html5/tabular-data.html#the-colgroup-element)
:   W3C Recommendation
[HTML 4.01](http://www.w3.org/TR/html401/struct/tables.html#edef-COLGROUP)
:   W3C Recommendation

## See also

### Related articles

#### HTML

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

-   **colgroup**

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

<!-- -->

    … further results

#### Tables

-   [border-collapse](/css/properties/border-collapse)

-   [border-spacing](/css/properties/border-spacing)

-   [caption-side](/css/properties/caption-side)

-   [empty-cells](/css/properties/empty-cells)

-   [Tables](/css/tables)

-   [col](/html/elements/col)

-   **colgroup**

-   [table](/html/elements/table)

-   [tbody](/html/elements/tbody)

-   [td](/html/elements/td)

-   [tfoot](/html/elements/tfoot)

-   [th](/html/elements/th)

-   `col`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

