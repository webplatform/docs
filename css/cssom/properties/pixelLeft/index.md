---
title: 'pixelLeft'
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
summary: 'Reflects the value of the Cascading Style Sheets (CSS) left attribute.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: css/cssom/properties/pixelLeft

---
## Summary

Reflects the value of the Cascading Style Sheets (CSS) left attribute.

Property of [css/cssom/properties](/css/cssom/properties)[css/cssom/properties](/css/cssom/properties)

## Syntax

``` js
var result = element.pixelLeft;
element.pixelLeft = value;
```

**Needs Examples**: This section should include examples.

## Notes

### Remarks

The **pixelLeft** property reflects the value of the Cascading Style Sheets (CSS) [**left**](/css/properties/left) attribute. Use the [**offsetLeft**](/dom/HTMLElement/offsetLeft) property to calculate actual positions within the document area. Unlike the [**left**](/css/properties/left) property, the **pixelLeft** value is an integer, not a string, and is always interpreted in pixels.

## See also

### Related pages

-   runtimeStyle[runtimeStyle](/css/cssom/runtimeStyle)
-   style[style](/css/cssom/style)
-   posLeft[posLeft](/css/cssom/properties/posLeft)
