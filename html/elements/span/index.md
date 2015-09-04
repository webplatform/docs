---
title: span
tags:
  - Markup
  - Elements
  - HTML
readiness: 'In Progress'
standardization_status: 'W3C Recommendation'
notes:
  - 'Events section must be modified.'
summary: 'Groups inline elements in a document. The span element is both style and semantics neutral; it does not assign any style attributes or semantic meaning on its own.'
uri: html/elements/span
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - HTML/Elements/text
    - HTML/Elements/c
    - Attributes/class
    - Attributes/lang
    - Attributes/bidi
    - Attributes/style

---
# span

## Summary

Groups inline elements in a document. The span element is both style and semantics neutral; it does not assign any style attributes or semantic meaning on its own.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLSpanElement](/dom/HTMLSpanElement)

## Examples

This example uses the **span** element to create an inline text container that changes the color of a word to blue.

``` {.html}
<p>This paragraph contains a single <span style="color: blue">blue</span> word.
```

This example uses the **span** element to add a simple [Microformats2 h-card](http://microformats.org/wiki/microformats2#h-card) to a person's name.

``` {.html}
<span class="h-card vcard">Pius Uzamere</span>
```

## Notes

### Remarks

The **SPAN** element is especially useful for applying cascading style sheets (CSS) styles.

### History

The span element was not initially part of HTML.

On July 3, 1995, Benjamin C. W. Sittler [proposes](http://lists.w3.org/Archives/Public/www-style/1995Jul/0003.html) a **generic text container tag** [\<text\>](/w/index.php?title=HTML/Elements/text&action=edit&redlink=1) for applying styles to certain blocks of text. The rendering is neutral except if used in conjunction of a stylesheet. There is a [debate](http://lists.w3.org/Archives/Public/www-style/1995Jul/thread.html#msg11) around [\<c\>](/w/index.php?title=HTML/Elements/c&action=edit&redlink=1) versus [\<text\>](/w/index.php?title=HTML/Elements/text&action=edit&redlink=1) about readability, meaning. Bert Bos is [mentioning](http://lists.w3.org/Archives/Public/www-style/1995Jul/0016.html) the extensibility nature of the [\<text\>](/w/index.php?title=HTML/Elements/text&action=edit&redlink=1) element through the [class](/w/index.php?title=Attributes/class&action=edit&redlink=1) attribute (with values such as city, person, date, etc.). Paul Prescod is [worried](http://lists.w3.org/Archives/Public/www-style/1995Jul/0017.html) that both elements will be abused. He is opposed to text mentionning that *"any new element should be on an old one"* and adding *"If we create a tag with no semantics it can be used anywehere without ever being wrong. We must force authors to properly tag the semantics of their document. We must force editor vendors to make that choice explicit in their interfaces."*

\<span\> has been introduced to html through the internationalization WG on September 25, 1995 in the [second draft html-i18n](http://tools.ietf.org/html/draft-ietf-html-i18n-01). The purpose was to create a generic container needed to carry the [lang](/w/index.php?title=Attributes/lang&action=edit&redlink=1) and [bidi](/w/index.php?title=Attributes/bidi&action=edit&redlink=1) attributes in cases where no other element is appropriate.

The [first draft of html-style](http://tools.ietf.org/html/draft-ietf-html-style-00) had the [\<c\>](/w/index.php?title=HTML/Elements/c&action=edit&redlink=1) element in its table of content with the purpose of applying a style to some text which doesn't have a structural role. Michael J Hannah on December 5, 1995 [proposes](http://lists.w3.org/Archives/Public/www-style/1995Dec/0039.html) to get rid of the new HTML element [\<c\>](/w/index.php?title=HTML/Elements/c&action=edit&redlink=1) to use the new element <span> part of the internationalization proposal [draft-ietf-html-i18n](http://tools.ietf.org/html/draft-ietf-html-i18n-01) because it will be able to carry the [style](/w/index.php?title=Attributes/style&action=edit&redlink=1) attribute. Then in the 23 January 1996 version of the [html-style](http://tools.ietf.org/html/draft-ietf-html-style-01) it has been replaced by the \<span\> element. </span>

But we had to wait until [HTML 4.01](http://www.w3.org/TR/html401/) to see the new element be [part of the HTML](http://www.w3.org/TR/html401/struct/global.html#edef-SPAN) language. It appears on the HTML 4 W3C Working Draft on September 17, 1997.

## Related specifications

Specification
:   Status
[HTML 5.1](http://www.w3.org/TR/html51/text-level-semantics.html#the-span-element)
:   W3C Working Draft
[HTML 5](http://www.w3.org/TR/html5/text-level-semantics.html#the-span-element)
:   W3C Recommendation
[HTML 4.01](http://www.w3.org/TR/html401/struct/global.html#edef-SPAN)
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

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

