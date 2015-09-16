---
title: 'b'
code_samples:
  - 'http://gist.github.com/7281844'
  - 'http://gist.github.com/321e5149c1e661e1de14'
compatibility:
  feature: b
  topic: html
notes:
  - 'Add compatibility.'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLElement](/dom/HTMLElement)'
readiness: 'In Progress'
standardization_status: 'W3C Candidate Recommendation'
summary: 'The b element represents a span of text to be stylistically offset from the normal prose without conveying any extra importance.'
tags:
  - Markup
  - Elements
  - HTML
  - XHTML
uri: html/elements/b

---
## Summary

The b element represents a span of text to be stylistically offset from the normal prose without conveying any extra importance.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLElement](/dom/HTMLElement)

It was originally used to tell the browser to make the enclosed text bold. While the **b** element is widely supported in browsers, its use is not recommended for this purpose since CSS can be used to achieve the same effect on a more semantically-appropriate element. In HTML5, **b** has been re-purposed to signify text this is offset in some way, but is of no greater significance than the surrounding text.

The **b** element should be used as a last resort when no other element is more appropriate, as it has no semantic value other than indicating that the contained text should be stylistically offset in some way (i.e. it’s like a shorter [**span** element](/html/elements/span)). For visually similar elements that do provide semantic meaning, consider [strong](/html/elements/strong), [dfn](/html/elements/dfn), [h1-h6](/html/elements/hn), or [abbr](/html/elements/abbr).

## Examples

In the following example, objects in a text adventure are highlighted as being special by use of the **b** element.

``` html
<p>You enter a small room. Your <b>sword</b> glows
brighter. A <b>rat</b> scurries past the corner wall.</p>
```

[View live example](http://code.webplatform.org/gist/7281844)

In this example, the **b** element is used to indicate both a company and a product name. Disambiguation via CSS is accomplished using the **class** attribute.

``` html
<p><b class="org">Acme <abbr title="Corporation">Corp</abbr></b>
is pleased to introduce the
<b class="product">Widget Blast 3000</b>.
This is a miracle of modern science that will
simplify your life, fry an egg, and even put
your kids to bed.</p>
```

[View live example](http://code.webplatform.org/gist/321e5149c1e661e1de14)

## Usage

     The b element makes a lot of sense for use as a wrapper for proper names (e.g. people, companies, products, locations) as they may be offset from the surrounding text in some way, but are not semantically meaningful.

Internationalization topics related to the **b** element:

-   [[b and i tags](http://www.w3.org/International/techniques/authoring-html#bandi%7CUsing)]

## Notes

As the **b** element has no inherent meaning, you should not use it to convey meaning; there is probably a more appropriate element for that. Headings should use the **h1** to **h6** elements, stress emphasis should use the **em** element, importance should be denoted with the **strong** element, and contextually-important/highlighted text should use the **mark** element.

## Related specifications

[HTML 5.1](http://www.w3.org/TR/html51/text-level-semantics.html#the-b-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/text-level-semantics.html#the-b-element)
:   W3C Recommendation

[HTML 4.01](http://www.w3.org/TR/html401/present/graphics.html#edef-B)
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

-   **b**

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

-   **b**

-   [b](/html/elements/b/ja)

-   [br](/html/elements/br)

-   [br](/html/elements/br/ja)

-   [caption](/html/elements/caption)

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
