---
title: type (SVGStyleElement)
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Unreviewed MSDN import'
readiness: 'Not Ready'
standardization_status: Unknown
tags:
  - SVG
uri: 'svg/properties/type (SVGStyleElement)'

---
## Notes

### Remarks

The **type** property specifies the style sheet language of the [**style**](/svg/elements/style) element's contents. The style sheet language is specified as a content type (for example, **"text/css"**).

If you do not provide a type, the value of **contentStyleType** on the [**svg**](/svg/elements/svg) element is used, which defaults to **"text/css"**. If a [**style**](/svg/elements/style) element falls outside of the outermost **svg** element and you do not provide the type, the value of **contentStyleType** on the **type** element defaults to **"text/css"**.

### Syntax

### Standards information

-   [Scalable Vector Graphics: Styling](http://go.microsoft.com/fwlink/p/?linkid=204734), Section 6.18.1

## See also

### Related pages (MSDN)

-   [**SVGStyleElement**](/svg/elements/style)
