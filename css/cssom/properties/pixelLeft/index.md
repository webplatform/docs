---
title: pixelLeft
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'In Progress'
notes:
  - 'Needs example, spec reference, standardization status'
summary: 'Reflects the value of the Cascading Style Sheets (CSS) left attribute.'
uri: css/cssom/properties/pixelLeft

---
# pixelLeft

## Summary

Reflects the value of the Cascading Style Sheets (CSS) left attribute.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[css/cssom/properties](/css/cssom/properties)</span></span>

## Syntax

``` {.js}
var result = element.pixelLeft;
element.pixelLeft = value;
```

**Needs Examples**: This section should include examples.

## Notes

### Remarks

The **pixelLeft** property reflects the value of the Cascading Style Sheets (CSS) [**left**](/css/properties/left) attribute. Use the [**offsetLeft**](/dom/HTMLElement/offsetLeft) property to calculate actual positions within the document area. Unlike the [**left**](/css/properties/left) property, the **pixelLeft** value is an integer, not a string, and is always interpreted in pixels.

## See also

### Related pages (MSDN)

-   `runtimeStyle`
-   `style`
-   `posLeft`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

