---
title: pre
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - "HTML information must be modified. Add compatibility.\nHow is whitespace/escaping handled when a 'code' tag is inside a 'pre' tag?"
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLPreElement](/dom/HTMLPreElement)'
readiness: 'Almost Ready'
standardization_status: 'W3C Recommendation'
summary: 'The pre tag defines preformatted text. Text in a pre element is displayed in a fixed-width font and preserves both spaces and line breaks.'
tags:
  - Markup
  - Elements
  - HTML
uri: html/elements/pre

---
## <span>Summary</span>

The pre tag defines preformatted text. Text in a pre element is displayed in a fixed-width font and preserves both spaces and line breaks.

## <span>Overview Table</span>

[DOM Interface](/dom/interface)
:   [HTMLPreElement](/dom/HTMLPreElement)

Examples of content might include:

-   e-mail
-   computer code
-   ASCII art
-   program output

This element is used with the code element, the samp element, or the kbd element, and so on, according to the kind of content inside a pre element.

## <span>Rendering in text/html</span>

Unlike in XML mode, a text/html parser will strip the newline character if it appears after the opening `<pre>` tag, as an authoring convenience.

## <span>Accessibility</span>

The author should consider accessibility, when use the pre element. This is because, when speech synthesizers, braille displays, and the like is used, there is a possibility that preformatted text is destroyed. For example, for cases like ASCII art, it is likely that an alternative presentation, such as a textual description, would be more universally accessible to the readers of the document.

## <span>Examples</span>

This example uses the **PRE** element to format text so that it renders exactly as it is typed.

``` html
<pre>
This text is formatted
   exactly
      as
         it
      is
   typed.
</pre>
```

Example of pre-formatted computer code inside a \<code\> tag

``` html

<pre>
  <code>
  process.run();
  </code>
</pre>

```

## <span>Usage</span>

     To cater for international users see: Managing text direction in form controls

## <span>Notes</span>

### <span>Remarks</span>

Text within the **PRE** element is formatted. Spaces and carriage returns are preserved.

## <span>Related specifications</span>

[HTML 5.1](http://www.w3.org/TR/html51/grouping-content.html#the-pre-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/grouping-content.html#the-pre-element)
:   W3C Recommendation

[HTML 4.01](http://www.w3.org/TR/html401/struct/text.html#edef-PRE)
:   W3C Recommendation

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `xmp`
