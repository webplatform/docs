---
title: getElementById
tags:
  - API
  - Object
  - Methods
  - DOM
  - Shadow
readiness: 'In Progress'
standardization_status: 'W3C Working Draft'
notes:
  - 'Needs spec reference, usage, example'
summary: 'Just like Document.getElementById except that it only works within the scope of this ShadowRoot''s shadow tree.'
uri: dom/shadowdom/ShadowRoot/getElementById

---
# getElementById

## Summary

Just like Document.getElementById except that it only works within the scope of this ShadowRoot's shadow tree.

*Method of [dom/shadowdom/ShadowRoot](/dom/shadowdom/ShadowRoot)*

## Syntax

``` {.js}
var result = element.getElementById();
```

## Return Value

Returns an object of type DOM Node.

Returns the DOM node specified by the given ID. Case matters, and if there is more than one node with the given ID, which node is returned is uncertain.

**Needs Examples**: This section should include examples.

