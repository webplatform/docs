---
title: filter
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Unreviewed MSDN import'
readiness: 'Not Ready'
standardization_status: Unknown
tags:
  - SVG
uri: svg/properties/filter

---
## Notes

### Remarks

[**Filter**](/svg/elements/filter) elements are never rendered directly; their only usage is as something that can be referenced using the **filter** property. Be aware that **filter** elements are available for referencing even when the [**display**](/css/properties/display) property on the **filter** element or any of its ancestors is set to **none**.

In the following example, a previously defined Gaussian\_Blur filter (that is, **filter:url(\#Gaussian\_Blur)"/\>**) is being applied to an SVG ellipse:

     <ellipse cx="200" cy="150" rx="70" ry="40" style="fill:#ff0000; stroke:#000000;
              stroke-width:2; filter:url(#Gaussian_Blur)"/>

### Syntax

## See also

### Related pages (MSDN)

-   [**CSSStyleDeclaration**](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)
-   [**Filter**](/svg/elements/filter)
