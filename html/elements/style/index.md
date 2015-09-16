---
title: style
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Add description/notes, compatibility.'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLStyleElement](/dom/HTMLStyleElement)'
readiness: 'In Progress'
summary: 'Defines style information for an HTML document. Inside the style element you specify how HTML elements should render in a browser. Each HTML document can contain multiple style tags.'
tags:
  - Pages
  - using
  - duplicate
  - arguments
  - in
  - template
  - calls
  - Markup
  - Elements
  - HTML
uri: html/elements/style

---
## Summary

Defines style information for an HTML document. Inside the style element you specify how HTML elements should render in a browser. Each HTML document can contain multiple style tags.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLStyleElement](/dom/HTMLStyleElement)

## Examples

This example encloses style declarations in the **STYLE** element and changes one of those settings using the **style** object.

``` html
<HEAD>
<STYLE>
   BODY {  background-color: white; color: black;  }
   H1 {  font: 8pt Arial bold;  }
   P  {  font: 10pt Arial; text-indent: 0.5in;  }
   A  {  text-decoration: none; color: blue;  }
</STYLE>
<SCRIPT>
    oParagraph.style.fontSize = 14;
</SCRIPT>
</HEAD>
<BODY>
<P>Sample Paragraph Text</P>
</BODY>
```

## Notes

### Remarks

The **STYLE** element should appear in the **HEAD** section of an HTML document. Microsoft Internet Explorer 4.0 and later permit multiple style blocks.

The **STYLE** element should appear in the **HEAD** section of an HTML document. Multiple style blocks are permitted.

### Standards information

-   [HTML 4.01 Specification](http://go.microsoft.com/fwlink/p/?linkid=25320), Section 14.2.3

### Members

The **style** object has these types of members:

-   [\#events Events]
-   [\#methods Methods]
-   [\#properties Properties]

#### Events

The **style** object has these events. {

## Related specifications

[HTML 5.1](http://www.w3.org/TR/html51/document-metadata.html#the-style-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/document-metadata.html#the-style-element)
:   W3C Recommendation

[HTML 4.01](http://www.w3.org/TR/html401/present/styles.html#edef-STYLE)
:   W3C Recommendation
