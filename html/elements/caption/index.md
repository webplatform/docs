---
title: 'caption'
code_samples:
  - 'http://gist.github.com/7282268'
compatibility:
  feature: caption
  topic: html
notes:
  - 'Add Category, Parent, Children and Compatibility information.'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLTableCaptionElement](/dom/HTMLTableCaptionElement)'
readiness: 'Almost Ready'
standardization_status: 'W3C Recommendation'
summary: 'The caption (&lt;caption&gt;) element represents the title of the table that is its parent.'
tags:
  - Markup
  - Elements
  - HTML
uri: html/elements/caption

---
## Summary

The caption (&lt;caption&gt;) element represents the title of the table that is its parent.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLTableCaptionElement](/dom/HTMLTableCaptionElement)

The **caption** element (\<caption\>) specifies a brief description for a table. The \<caption\> element must be inserted immediately after the \<table\> element.

## Examples

This example uses the **caption** element to provide a brief description for a table.

``` html

<table>
 <caption>Characteristics with positive and negative sides</caption>
 <thead>
  <tr>
   <th>Characteristic</th>
   <th>Negative</th>
   <th>Positive</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <th>Mood</th>
   <td>Sad</td>
   <td>Happy</td>
  </tr>
  <tr>
   <th>Grade</th>
   <td>Failing</td>
   <td>Passing</td>
  </tr>
 </tbody>
</table>

```

[View live example](http://code.webplatform.org/gist/7282268)

## Notes

### Remarks

The **caption** element should be a child of the \<table\> element.

A caption can introduce context for a table, making it significantly easier to understand.

When a table element is the only content in a figure element other than the **figcaption**, the caption element should be omitted in favor of the [figcaption](/html/elements/figcaption).

## Related specifications

[HTML 5.1](http://www.w3.org/TR/html51/tabular-data.html#the-caption-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/tabular-data.html#the-caption-element)
:   W3C Recommendation

[HTML 4.01](http://www.w3.org/TR/html401/struct/tables.html#edef-CAPTION)
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

-   **caption**

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

-   [th](/html/elements/th)

-   [time](/html/elements/time)

#### Text

-   [block-progression](/css/properties/block-progression)

-   [font-language-override](/css/properties/font-language-override)

-   [font-size](/css/properties/font-size)

-   [hyphenate-limit-chars](/css/properties/hyphenate-limit-chars)

-   [hyphenate-limit-lines](/css/properties/hyphenate-limit-lines)

-   [hyphenate-limit-zone](/css/properties/hyphenate-limit-zone)

-   [hyphens](/css/properties/hyphens)

-   [ime-mode](/css/properties/ime-mode)

-   [layout-grid](/css/properties/layout-grid)

-   [layout-grid-char](/css/properties/layout-grid-char)

-   [layout-grid-line](/css/properties/layout-grid-line)

-   [layout-grid-mode](/css/properties/layout-grid-mode)

-   [layout-grid-type](/css/properties/layout-grid-type)

-   [letter-spacing](/css/properties/letter-spacing)

-   [text-overflow-ellipsis](/css/properties/text-overflow-ellipsis)

-   [text-overflow-mode](/css/properties/text-overflow-mode)

-   [text-rendering](/css/properties/text-rendering)

-   [user-modify](/css/properties/user-modify)

-   [Text](/css/text)

-   [size](/html/attributes/size)

-   [b](/html/elements/b)

-   [b](/html/elements/b/ja)

-   [br](/html/elements/br)

-   [br](/html/elements/br/ja)

-   **caption**

-   [cite](/html/elements/cite)

-   [code](/html/elements/code)

-   [del](/html/elements/del)

-   [dfn](/html/elements/dfn)

-   [em](/html/elements/em)

-   [font](/html/elements/font)

-   [hr](/html/elements/hr)

-   [i](/html/elements/i)

-   [ins](/html/elements/ins)

-   [kbd](/html/elements/kbd)

-   [mark](/html/elements/mark)

-   [samp](/html/elements/samp)

-   [strong](/html/elements/strong)

-   [Achieving typographic effects with the canvas tag](/tutorials/canvas_texteffects)

### External resources

<http://www.w3.org/wiki/HTML/Elements/caption>
