---
title: getElementsByTagName
tags:
  - API
  - Object
  - Methods
  - DOM
  - Shadow
readiness: 'In Progress'
standardization_status: 'W3C Editor''s Draft'
notes:
  - 'Needs spec reference, example'
summary: 'Just like Document/getElementsByTagName except that it only works within the scope of this ShadowRoot''s shadow tree.'
uri: dom/shadowdom/ShadowRoot/getElementsByTagName

---
# getElementsByTagName

## Summary

Just like Document/getElementsByTagName except that it only works within the scope of this ShadowRoot's shadow tree.

*Method of [dom/shadowdom/ShadowRoot](/dom/shadowdom/ShadowRoot)*

## Syntax

``` {.js}
var result = element.getElementsByTagName(name);
```

## Parameters

### name

 Data-typeÂ
:   String

 The name of the element's tag.

## Return Value

Returns an object of type DOM Node.

A DOM collection of elements with the given name.

**Needs Examples**: This section should include examples.

