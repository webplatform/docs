---
title: 'pixelRight'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs example, spec reference, standardization status'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: css/cssom/properties
    href: /css/cssom/properties
summary: 'Reflects the value of the Cascading Style Sheets (CSS) right attribute.'
tags:
  - API_Object_Properties
  - DOM
  - Needs_Examples
uri: css/cssom/properties/pixelRight

---
## Summary

Reflects the value of the Cascading Style Sheets (CSS) right attribute.

Property of [css/cssom/properties](/css/cssom/properties)[css/cssom/properties](/css/cssom/properties)

## Syntax

``` js
var result = element.pixelRight;
element.pixelRight = value;
```

## Notes

### Remarks

The **pixelRight** property reflects the value of the Cascading Style Sheets (CSS) [**right**](/css/properties/right) attribute. Unlike the [**right**](/css/properties/right) property, the **pixelRight** value is an integer, not a string, and is always interpreted in pixels.

## See also

### Related pages

-   runtimeStyle[runtimeStyle](/css/cssom/runtimeStyle)
-   style[style](/css/cssom/style)
-   posRight[posRight](/css/cssom/properties/posRight)
