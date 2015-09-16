---
title: ins
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/6365735'
notes:
  - 'Add Compatibility'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLModElement](/dom/HTMLModElement)'
readiness: 'In Progress'
standardization_status: 'W3C Recommendation'
summary: 'The ins element represents a range of text that has been inserted (added) into a document.'
tags:
  - Markup
  - Elements
  - HTML
  - XHTML
uri: html/elements/ins

---
## Summary

The ins element represents a range of text that has been inserted (added) into a document.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLModElement](/dom/HTMLModElement)

### Attributes

Besides the [global attributes](/html/global_attributes) the following attributes are supported:

[**cite**](/html/attributes/cite)
:   The **cite** attribute may be used to specify the address of a document that explains the change. When that document is long (e.g. the minutes of a meeting) authors are encouraged to include a fragment identifier pointing to the specific part of that document that discusses the change.
[**datetime**](/html/attributes/datetime)
:   The **datetime** attribute may be used to specify the time and date of the change. If present, it must be a valid [date string with optional time](http://www.w3.org/html/wg/drafts/html/master/infrastructure.html#valid-date-string-with-optional-time).

## Examples

This example uses the **ins** element to specify text inserted into a document.

``` html
<p>This text existed in the document when it
was written. <ins datetime="1997-10-01T12:15:30-05:00">This
text was inserted on 1 October 1997 at 12:15pm in
the Eastern time zone.</ins></p>
```

This example uses **ins** and **del** elements to explain changes in a document

``` html
<p>I <del>am</del><ins>was</ins> on vacation in <del>France</del><ins>Italy</ins>.</p>
<p>
  <del>It is supposed to be sunny and hot.</del>
  <ins>It rained in France so we decided to go to Italy instead.</ins>
</p>
```

[View live example](http://code.webplatform.org/gist/6365735)

## Usage

     The default behavior of the ins element is as a phrasing-level element, but it can be wrapped around any element within the body.

## Notes

The default browser display of **ins** is underlined.

If you want to underline text, but it is not an insertion, you should use the CSS rule **text-decoration: underline** on the appropriate element enclosing the text.

If you are looking to emphasize a word or phrase, the [**em** element](/html/elements/em) would be a better choice.

For Internet Explorer 8 and later the value of the [**cite**](/html/attributes/cite) attribute depends on the current document compatibility mode.

## Related specifications

[HTML 5.1](http://www.w3.org/TR/html51/edits.html#the-ins-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/edits.html#the-ins-element)
:   W3C Recommendation

[HTML 4.01](http://www.w3.org/TR/html401/struct/text.html#edef-ins)
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

-   **ins**

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

-   [dfn](/html/elements/dfn)

-   [em](/html/elements/em)

-   [font](/html/elements/font)

-   [hr](/html/elements/hr)

-   [i](/html/elements/i)

-   **ins**

-   [kbd](/html/elements/kbd)

-   [mark](/html/elements/mark)

-   [samp](/html/elements/samp)

-   [strong](/html/elements/strong)

-   [Achieving typographic effects with the canvas tag](/tutorials/canvas_texteffects)

### Other articles

-   **ins**
-   [del](/html/elements/del)

### External resources

-   [Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/HTML/Element/ins)
-   [Microsoft Developer Network](http://msdn.microsoft.com/en-us/library/ie/ms535842%28v=vs.85%29.aspx)
-   <http://www.w3.org/TR/html-markup/ins.html#ins>
