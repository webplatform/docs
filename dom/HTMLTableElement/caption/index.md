---
title: caption
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - compatibility
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/HTMLTableElement
    href: /dom/HTMLTableElement
  return:
    predicate: 'Returns an object of type '
    value: 'DOM Node'
    href: /dom/HTMLTableElement
standardization_status: 'W3C Recommendation'
summary: 'Gets or sets the caption element of a table.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/HTMLTableElement/caption

---
## <span>Summary</span>

Gets or sets the caption element of a table.

Property of [dom/HTMLTableElement](/dom/HTMLTableElement)[dom/HTMLTableElement](/dom/HTMLTableElement)

## <span>Syntax</span>

``` js
var captionElement = table.caption;
table.caption = newCaption;
```

## <span>Return Value</span>

Returns an object of type DOM NodeDOM Node

The caption element, or null.

## <span>Examples</span>

This example sets the inline style for the **caption** property.

``` js
document.getElementById("mytable").caption.style.color = "blue";
```

## <span>Notes</span>

If a table contains multiple captions, this property returns the first one.

## <span>Related specifications</span>

[DOM Level 1](http://www.w3.org/TR/REC-DOM-Level-1/)
:   Recommendation
