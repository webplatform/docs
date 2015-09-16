---
title: s – strikethrough
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/604bc1947f655fb863a1'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLElement](/dom/HTMLElement)'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'The s element represents contents that are no longer accurate and must be marked accordingly in order to allow keeping it in the document.'
tags:
  - Markup
  - Elements
  - HTML
uri: html/elements/s

---
## s

For technical reasons, the title of this article is not the text used to call this API. Instead, use `s`

## Summary

The s element represents contents that are no longer accurate and must be marked accordingly in order to allow keeping it in the document.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLElement](/dom/HTMLElement)

Use the **s** element to represent things that are no longer relevant or no longer accurate. However, **s** is not appropriate when indicating document edits; for that, use the [**del**](/html/elements/del) and [**ins**](/html/elements/ins) elements, as appropriate.

## Examples

This example uses the `<s>` element to render a text that no longer accurate.

``` html
<ul>
  <li><s>today's special: Gouda Cheeseburger, .14</s> SOLD OUT</li>
  <li>Classic Cheeseburger, .50</li>
</ul>
```

[View live example](http://code.webplatform.org/gist/604bc1947f655fb863a1)

Typical browser default CSS properties for the `<s>` element.

``` css
text-decoration: line-through;
```

## Usage

     While s and del appear to be similar, namely marking obsolete content, but they differ in semantics. del marks text that has been removed from the document, but s marks text that is to be kept in the document, but made clear that its content is no longer accurate.

## Notes

The information that the text inside the **s** element is not accurate is not indicated to assistive technologies, like screen readers. Instead it is interpreted like regular text which can lead to confusion. Add clear text that the information is invalid.

## Related specifications

[HTML 5.1](http://www.w3.org/TR/html51/text-level-semantics.html#the-s-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/text-level-semantics.html#the-s-element)
:   W3C Recommendation

[HTML 4.01](http://www.w3.org/TR/html401/present/graphics.html#edef-S)
:   W3C Recommendation

## See also

### Other articles

-   [`ins`](/html/elements/ins)
-   [`del`](/html/elements/del)
-   [`strike`](/html/elements/strike)

### External resources

-   [Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/HTML/Element/s)
-   [Microsoft Developer Network](http://msdn.microsoft.com/en-us/library/ie/ms535890%28v=vs.85%29.aspx)
-   <http://www.w3.org/TR/html-markup/s.html#s>
