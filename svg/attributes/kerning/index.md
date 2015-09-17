---
title: 'kerning'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: kerning
  topic: svg
notes:
  - 'Needs all content'
readiness: 'Not Ready'
tags:
  - Markup_Attributes
  - SVG
  - Needs_Summary
  - Needs_Examples
uri: svg/attributes/kerning

---
<table class="wikitable">
<tr>
<th>
Applies to

</th>
<td>
 ?

</td>
</tr>
</table>
## Notes

### Remarks

When a **length** is provided, its value is added to the inter-character spacing value specified by the [**letterSpacing**](/css/properties/letter-spacing) property. If a **length** is provided without a unit identifier (for example, an unqualified number such as 128), Internet Explorer processes the **length** as a width value.

### Syntax

    kerning: auto | length | inherit

### Standards information

-   [Scalable Vector Graphics: Text](http://go.microsoft.com/fwlink/p/?linkid=199818), Section 10.11

## See also

### Related pages

-   [**CSSStyleDeclaration**](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)
-   [**currentStyle**](/css/cssom/currentStyle)
-   [**style**](/css/cssom/style)
-   [**SVGTSpanElement**](/svg/elements/tspan)
-   [**SVGTextPathElement**](/svg/elements/textPath)
-   [**SVGTextElement**](/svg/elements/text)

### Reference

-   [**letterSpacing**](/css/properties/letter-spacing)
-   [**wordSpacing**](/css/text/word-spacing/word-spacing)
