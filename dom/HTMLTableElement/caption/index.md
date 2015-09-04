---
title: caption
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Almost Ready'
standardization_status: 'W3C Recommendation'
notes:
  - compatibility
summary: 'Gets or sets the caption element of a table.'
uri: dom/HTMLTableElement/caption

---
# caption

## Summary

Gets or sets the caption element of a table.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/HTMLTableElement](/dom/HTMLTableElement)</span></span>

## Syntax

``` {.js}
var captionElement = table.caption;
table.caption = newCaption;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">DOM Node</span></span>

The caption element, or null.

## Examples

This example sets the inline style for the **caption** property.

``` {.js}
document.getElementById("mytable").caption.style.color = "blue";
```

## Notes

If a table contains multiple captions, this property returns the first one.

## Related specifications

Specification
:   Status
[DOM Level 1](http://www.w3.org/TR/REC-DOM-Level-1/)
:   Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

