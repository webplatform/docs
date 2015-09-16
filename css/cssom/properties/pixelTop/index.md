---
title: 'pixelTop'
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
summary: 'Reflects the value of the Cascading Style Sheets (CSS) top attribute.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: css/cssom/properties/pixelTop

---
## Summary

Reflects the value of the Cascading Style Sheets (CSS) top attribute.

Property of [css/cssom/properties](/css/cssom/properties)[css/cssom/properties](/css/cssom/properties)

## Syntax

``` js
var result = element.pixelTop;
element.pixelTop = value;
```

**Needs Examples**: This section should include examples.

## Notes

### Remarks

The **pixelTop** property reflects the value of the Cascading Style Sheets (CSS) [**top**](/css/properties/top) attribute. Use the [**offsetTop**](/dom/HTMLElement/offsetTop) property to calculate actual positions within the document area. Unlike the [**top**](/css/properties/top) property, the **pixelTop** value is an integer, not a string, and is always interpreted in pixels.

## See also

### Related pages

-   runtimeStyle[runtimeStyle](/css/cssom/runtimeStyle)
-   style[style](/css/cssom/style)
-   posTop[posTop](/css/cssom/properties/posTop)
