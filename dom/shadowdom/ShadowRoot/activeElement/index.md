---
title: activeElement
tags:
  0: API
  1: Object
  2: Properties
  4: DOM
  5: Shadow
readiness: 'In Progress'
standardization_status: 'W3C Editor''s Draft'
notes:
  - 'Needs spec reference, example'
summary: 'Represents the currently focused element in the shadow tree.'
uri: dom/shadowdom/ShadowRoot/activeElement

---
# activeElement

## Summary

Represents the currently focused element in the shadow tree.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/shadowdom/ShadowRoot](/dom/shadowdom/ShadowRoot)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = element.activeElement;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Element</span></span>

On getting, the attribute must return the currently focused element in the shadow tree or null, if there is none.

**Needs Examples**: This section should include examples.

