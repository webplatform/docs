---
title: 'pre'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: pre
  topic: html
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
## Summary

The pre tag defines preformatted text. Text in a pre element is displayed in a fixed-width font and preserves both spaces and line breaks.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLPreElement](/dom/HTMLPreElement)

Examples of content might include:

-   e-mail
-   computer code
-   ASCII art
-   program output

This element is used with the code element, the samp element, or the kbd element, and so on, according to the kind of content inside a pre element.

## Rendering in text/html

Unlike in XML mode, a text/html parser will strip the newline character if it appears after the opening `<pre>` tag, as an authoring convenience.

## Accessibility

The author should consider accessibility, when use the pre element. This is because, when speech synthesizers, braille displays, and the like is used, there is a possibility that preformatted text is destroyed. For example, for cases like ASCII art, it is likely that an alternative presentation, such as a textual description, would be more universally accessible to the readers of the document.

## Examples

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

## Usage

     To cater for international users see: Managing text direction in form controls

## Notes

### Remarks

Text within the **PRE** element is formatted. Spaces and carriage returns are preserved.

## Related specifications

[HTML 5.1](http://www.w3.org/TR/html51/grouping-content.html#the-pre-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/grouping-content.html#the-pre-element)
:   W3C Recommendation

[HTML 4.01](http://www.w3.org/TR/html401/struct/text.html#edef-PRE)
:   W3C Recommendation

## See also

### Related pages

-   `xmp`
