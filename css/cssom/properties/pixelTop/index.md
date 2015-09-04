---
title: pixelTop
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'In Progress'
notes:
  - 'Needs example, spec reference, standardization status'
summary: 'Reflects the value of the Cascading Style Sheets (CSS) top attribute.'
uri: css/cssom/properties/pixelTop

---
# pixelTop

## Summary

Reflects the value of the Cascading Style Sheets (CSS) top attribute.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[css/cssom/properties](/css/cssom/properties)</span></span>

## Syntax

``` {.js}
var result = element.pixelTop;
element.pixelTop = value;
```

**Needs Examples**: This section should include examples.

## Notes

### Remarks

The **pixelTop** property reflects the value of the Cascading Style Sheets (CSS) [**top**](/css/properties/top) attribute. Use the [**offsetTop**](/dom/HTMLElement/offsetTop) property to calculate actual positions within the document area. Unlike the [**top**](/css/properties/top) property, the **pixelTop** value is an integer, not a string, and is always interpreted in pixels.

## See also

### Related pages (MSDN)

-   `runtimeStyle`
-   `style`
-   `posTop`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

