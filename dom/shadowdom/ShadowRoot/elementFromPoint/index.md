---
title: elementFromPoint
tags:
  0: API
  1: Object
  2: Methods
  4: DOM
  5: Shadow
readiness: 'In Progress'
standardization_status: 'W3C Editor''s Draft'
notes:
  - 'Needs spec reference, example'
summary: 'Returns an element at specified coordinates.'
uri: dom/shadowdom/ShadowRoot/elementFromPoint

---
# elementFromPoint

## Summary

Returns an element at specified coordinates.

*Method of [dom/shadowdom/ShadowRoot](/dom/shadowdom/ShadowRoot)*

## Syntax

``` {.js}
var result = element.elementFromPoint(x, y);
```

## Parameters

### x

 Data-typeÂ
:   String

 The horizontal position of the element. May not be negative.

### y

 Data-typeÂ
:   String

 The vertical position of the element. May not be negative.

## Return Value

Returns an object of type Element.

If x is greater than the viewport width or if y is greater than the viewport height, excluding the size of any rendered scrollbars, returns null.

**Needs Examples**: This section should include examples.

