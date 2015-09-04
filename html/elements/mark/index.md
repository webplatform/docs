---
title: mark
tags:
  - Markup
  - Elements
  - HTML
readiness: 'In Progress'
notes:
  - 'Add Category, Parent, Children and Compatibility information. Add HTML information section.'
summary: 'Represents a run of text that is contextually-important for some reason, such as text that has been marked or highlighted.'
uri: html/elements/mark

---
# mark

## Summary

Represents a run of text that is contextually-important for some reason, such as text that has been marked or highlighted.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLElement](/dom/HTMLElement)

## Examples

The following example shows the difference between denoting the importance of a span of text (**strong**) as opposed to denoting the relevance of a span of text (**mark**). It is an extract from a textbook, where the extract has had the parts relevant to the exam highlighted. The safety warnings, important though they may be, are not relevant to the exam.

``` {.html}
<h3>Wormhole Physics Introduction</h3>
<p><mark>A wormhole in normal conditions can be held open for a
maximum of just under 39 minutes.</mark> Conditions that can increase
the time include a powerful energy source coupled to one or both of
the gates connecting the wormhole, and a large gravity well (such as a
black hole).</p>
<p><mark>Momentum is preserved across the wormhole. Electromagnetic
radiation can travel in both directions through a wormhole,
but matter cannot.</mark></p>
<p>When a wormhole is created, a vortex normally forms.
<strong>Warning: The vortex caused by the wormhole opening will
annihilate anything in its path.</strong> Vortexes can be avoided when
using sufficiently advanced dialing technology.</p>
<p><mark>An obstruction in a gate will prevent it from accepting a
wormhole connection.</mark></p>
```

This example uses mark to indicate the "current" link.

``` {.html}
<nav>
  <ul>
    <li><a href="/one">One</a></li>
    <li><mark><a href="/two">Two</a></mark></li>
    <li><a href="/three">Three</a></li>
    <li><a href="/four">Four</a></li>
  </ul>
<nav>
```

## Usage

     The mark element is a phrasing-level element. It must not contain block-level elements, but it can contain other phrasing-level elements.

## Notes

The **mark** element denotes the relevance of a span of text. By default, most browsers render it in black text on a yellow background, but you can change that with CSS.

To indicate importance, use [**strong**](/html/elements/em); for emphasis, use [**em**](/html/elements/em).

When used in the main prose of a document, the **mark** element indicates a part of the document that has been highlighted. When used in a quotation or other block of text (such as an [**aside**](/html/elements/aside)), it indicates a highlight that was not originally present but which has been added to bring the reader's attention to a part of the text. For example, the following are valid uses for the **mark** element:

-   Bring attention to a particular string of text.
-   Highlight parts of document that match a search string.
-   Enable body text to refer to a specific part of a quotation or code fragment.

Windows Internet Explorer 9. The **mark** element is only supported for webpages displayed in IE9 Standards mode. For more information, see Defining Document Compatibility.

## Related specifications

Specification
:   Status
[HTML 5.1](http://www.w3.org/TR/html51/text-level-semantics.html#the-mark-element)
:   W3C Working Draft
[HTML 5](http://www.w3.org/TR/html5/text-level-semantics.html#the-mark-element)
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

<!-- -->

    … further results

#### Text

-   [block-progression](/css/properties/block-progression)

-   [font-language-override](/css/properties/font-language-override)

-   [font-size](/css/properties/font-size)

-   [font-synthesis](/css/properties/font-synthesis)

-   [hanging-punctuation](/css/properties/hanging-punctuation)

-   [hyphenate-limit-chars](/css/properties/hyphenate-limit-chars)

-   [hyphenate-limit-lines](/css/properties/hyphenate-limit-lines)

-   [hyphenate-limit-zone](/css/properties/hyphenate-limit-zone)

-   [hyphens](/css/properties/hyphens)

-   [ime-mode](/css/properties/ime-mode)

-   [layout-flow](/css/properties/layout-flow)

-   [layout-grid](/css/properties/layout-grid)

-   [layout-grid-char](/css/properties/layout-grid-char)

-   [layout-grid-line](/css/properties/layout-grid-line)

-   [layout-grid-mode](/css/properties/layout-grid-mode)

-   [layout-grid-type](/css/properties/layout-grid-type)

-   [letter-spacing](/css/properties/letter-spacing)

-   [line-break](/css/properties/line-break)

-   [max-font-size](/css/properties/max-font-size)

-   [min-font-size](/css/properties/min-font-size)

-   [text-overflow-ellipsis](/css/properties/text-overflow-ellipsis)

-   [text-overflow-mode](/css/properties/text-overflow-mode)

-   [text-rendering](/css/properties/text-rendering)

-   [text-underline-position](/css/properties/text-underline-position)

-   [text-underline-style](/css/properties/text-underline-style)

-   [text-underline-width](/css/properties/text-underline-width)

-   [user-input](/css/properties/user-input)

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

-   [dfn](/html/elements/dfn)

-   [em](/html/elements/em)

-   [font](/html/elements/font)

-   [hr](/html/elements/hr)

-   [i](/html/elements/i)

-   [ins](/html/elements/ins)

-   [kbd](/html/elements/kbd)

-   **mark**

-   [samp](/html/elements/samp)

-   [strong](/html/elements/strong)

-   [Achieving typographic effects with the canvas tag](/tutorials/canvas_texteffects)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

