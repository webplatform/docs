---
title: 'dfn'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: dfn
  topic: html
notes:
  - 'Add Category, Parent, Children and Compatibility information.'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLElement](/dom/HTMLElement)'
readiness: 'In Progress'
summary: 'The dfn element indicates the defining instance of a term.'
tags:
  - Markup_Elements
  - HTML
  - XHTML
uri: html/elements/dfn

---
## Summary

The dfn element indicates the defining instance of a term.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLElement](/dom/HTMLElement)

-   If the dfn element is specified, nearest parent of the dfn element(paragraph, description list group, or section) must also contain the definitions for the defining term.
-   The priority level of defining term is as follow:
    1.  Value of the title attribute in the dfn element.
    2.  Value of the title attribute in the abbr element. (if the dfn element contains exactly one element child node and no child text nodes, and that child element is the abbr element
    3.  TextContent of the dfn element
-   If the title attribute of the dfn element is present, then it must contain only the term being defined.

## Examples

This example uses the **dfn** element to indicate the defining instance of a new term.

``` html
<p>The <dfn title="Garage Door Opener">GDO</dfn>
is a device that allows off-world teams to open the iris.</p>
```

This example uses the **dfn** element to indicate the defining instance of a new term that is an abbreviation.

``` html
<p>The <dfn><abbr title="Garage Door Opener">GDO</abbr></dfn>
is a device that allows off-world teams to open the iris.</p>
<!-- ... later in the document: -->
<p>Teal'c activated his <abbr>GDO</abbr>
and so Hammond ordered the iris to be opened.</p>
```

This example uses the **dfn** element to indicate the defining instance of a new term and then uses an anchor to provide a reference to that instance.

``` html
<p>The <dfn id="dfn-gdo"><abbr title="Garage Door Opener">GDO</abbr></dfn>
is a device that allows off-world teams to open the iris.</p>
<!-- ... later in the document: -->
<p>Teal'c activated his <a href="#dfn-gdo"><abbr>GDO</abbr></a>
and so Hammond ordered the iris to be opened.</p>
```

## Usage

     The dfn is a phrasing-level element and can’t contain block-level elements, but it can contain other phrasing type elements like abbr, read on…

If the **dfn** element has a [**title** attribute](/html/attributes/title), then the value of that attribute serves as the definition for the text inside the element (see Example 1).

If the **dfn** contains exactly one child element (and no other text) //and// that child element is an [**abbr** element](/html/elements/abbr) with a [**title** attribute](/html/attributes/title), then the exact value of that **title** attribute serves as the definition for the text inside the **abbr** (see Example 2).

If the **dfn** only contains text, the exact text content of the element gives the term being defined.

If the [**title** attribute](/html/attributes/title) of the **dfn** element is present, then it must contain only the definition of the term being defined.

## Notes

If given an [**id** attribute](/html/attributes/id), a **dfn** may serve as a reference for other elements on the page by anchoring to the **dfn** (see Example 3).

## Related specifications

[HTML 5.1](http://www.w3.org/TR/html51/text-level-semantics.html#the-dfn-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/text-level-semantics.html#the-dfn-element)
:   W3C Recommendation

[HTML 4.01](http://www.w3.org/TR/html401/struct/text.html#edef-DFN)
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

-   **dfn**

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

-   [caption](/html/elements/caption)

-   [cite](/html/elements/cite)

-   [code](/html/elements/code)

-   [del](/html/elements/del)

-   **dfn**

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

### Other articles

-   acronym[acronym](/html/elements/acronym)
-   address[address](/html/elements/address)
-   cite[cite](/html/elements/cite)
-   i[i](/html/elements/i)
