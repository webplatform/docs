---
title: 'getElementsByTagName'
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
    value: 'DOM Node'
    href: /dom/shadowdom/ShadowRoot
standardization_status: 'W3C Editor''s Draft'
summary: 'Just like Document/getElementsByTagName except that it only works within the scope of this ShadowRoot''s shadow tree.'
tags:
  - API_Object_Methods
  - DOM
  - Shadow_DOM
  - Needs_Examples
uri: dom/shadowdom/ShadowRoot/getElementsByTagName

---
## Summary

Just like Document/getElementsByTagName except that it only works within the scope of this ShadowRoot's shadow tree.

Method of [dom/shadowdom/ShadowRoot](/dom/shadowdom/ShadowRoot)[dom/shadowdom/ShadowRoot](/dom/shadowdom/ShadowRoot)

## Syntax

``` js
var result = element.getElementsByTagName(name);
```

## Parameters

### name

 Data-type
:   String

 The name of the element's tag.

## Return Value

Returns an object of type DOM NodeDOM Node

A DOM collection of elements with the given name.
