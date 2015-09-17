---
title: 'getElementById'
notes:
  - 'Needs spec reference, usage, example'
readiness: 'In Progress'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/shadowdom/ShadowRoot
    href: /dom/shadowdom/ShadowRoot
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/shadowdom/ShadowRoot
standardization_status: 'W3C Working Draft'
summary: 'Just like Document.getElementById except that it only works within the scope of this ShadowRoot''s shadow tree.'
tags:
  - API_Object_Methods
  - DOM
  - Shadow_DOM
  - Needs_Examples
uri: dom/shadowdom/ShadowRoot/getElementById

---
## Summary

Just like Document.getElementById except that it only works within the scope of this ShadowRoot's shadow tree.

Method of [dom/shadowdom/ShadowRoot](/dom/shadowdom/ShadowRoot)[dom/shadowdom/ShadowRoot](/dom/shadowdom/ShadowRoot)

## Syntax

``` js
var result = element.getElementById();
```

## Return Value

Returns an object of type DOM NodeDOM Node

Returns the DOM node specified by the given ID. Case matters, and if there is more than one node with the given ID, which node is returned is uncertain.
