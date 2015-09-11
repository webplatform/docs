---
title: q – quote
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Add description/notes, compatibility.'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLQuoteElement](/dom/HTMLQuoteElement)'
readiness: 'Almost Ready'
standardization_status: 'W3C Recommendation'
summary: 'The q element represents some phrasing content quoted from another source.'
tags:
  - Markup
  - Elements
  - HTML
  - Usability
uri: html/elements/q

---
## <span>q</span>

For technical reasons, the title of this article is not the text used to call this API. Instead, use `q`

## <span>Summary</span>

The q element represents some phrasing content quoted from another source.

## <span>Overview Table</span>

[DOM Interface](/dom/interface)
:   [HTMLQuoteElement](/dom/HTMLQuoteElement)

Do not use quote characters (`'`, `"`, ``` `` ```, etc) when using the **q** element. If used with the [html/elements/cite](/html/elements/cite) element, the cite must contain a valid url.

## <span>Attributes</span>

-   `cite` = valid URL potentially surrounded by spaces
    Specifies the address in the quotation source. [[Example B]](#Example_B)

## <span>Examples</span>

This example uses the **q** element to set apart a quotation in text.

``` html
<p>She then said, <q>See you around, kiddo!</q></p>
```

This example shows that the **q** element can have child elements.

``` html
<p>Chicken Little: <q>The sky is falling…
the sky is falling… <em>the sky is falling!</em></q></p>
```

## <span>Usage</span>

     The q should be used to denote short, inline quotes that do not need a paragraph of their own.

For longer quotes, please use the [**blockquote**](/html/elements/blockquote) element.

## <span>Related specifications</span>

[HTML 5.1](http://www.w3.org/TR/html51/text-level-semantics.html#the-q-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/text-level-semantics.html#the-q-element)
:   W3C Recommendation

[HTML 4.01](http://www.w3.org/TR/html401/struct/text.html#edef-Q)
:   W3C Recommendation

## <span>See also</span>

### <span>Other articles</span>

-   [`cite`](/html/elements/cite)
-   [`blockquote`](/html/elements/blockquote)
