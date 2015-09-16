---
title: elementFromPoint
notes:
  - 'Needs spec reference, example'
readiness: 'In Progress'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/shadowdom/ShadowRoot
    href: /dom/shadowdom/ShadowRoot
  return_type:
    predicate: 'Returns an object of type  '
    value: Element
    href: /dom/shadowdom/ShadowRoot
standardization_status: 'W3C Editor''s Draft'
summary: 'Returns an element at specified coordinates.'
tags:
  0: API
  1: Object
  2: Methods
  4: DOM
  5: Shadow
uri: dom/shadowdom/ShadowRoot/elementFromPoint

---
## Summary

Returns an element at specified coordinates.

Method of [dom/shadowdom/ShadowRoot](/dom/shadowdom/ShadowRoot)[dom/shadowdom/ShadowRoot](/dom/shadowdom/ShadowRoot)

## Syntax

``` js
var result = element.elementFromPoint(x, y);
```

## Parameters

### x

 Data-type
:   String

 The horizontal position of the element. May not be negative.

### y

 Data-type
:   String

 The vertical position of the element. May not be negative.

## Return Value

Returns an object of type ElementElement

If x is greater than the viewport width or if y is greater than the viewport height, excluding the size of any rendered scrollbars, returns null.

**Needs Examples**: This section should include examples.

