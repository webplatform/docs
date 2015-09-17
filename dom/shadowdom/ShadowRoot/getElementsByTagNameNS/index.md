---
title: 'getElementsByTagNameNS'
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
summary: 'Just like document.getElementsByTagNameNS except that it only works within the scope of this ShadowRoot''s shadow tree.'
tags:
  - API_Object_Methods
  - DOM
  - Shadow_DOM
  - Needs_Examples
uri: dom/shadowdom/ShadowRoot/getElementsByTagNameNS

---
## Summary

Just like document.getElementsByTagNameNS except that it only works within the scope of this ShadowRoot's shadow tree.

Method of [dom/shadowdom/ShadowRoot](/dom/shadowdom/ShadowRoot)[dom/shadowdom/ShadowRoot](/dom/shadowdom/ShadowRoot)

## Syntax

``` js
var result = element.getElementsByTagNameNS(pvarNS, bstrLocalName);
```

## Parameters

### pvarNS

 Data-type
:   VARIANT

 The namespace URI that defines the desired elements or an asterisk (\*) to match all namespaces with the document.

### bstrLocalName

 Data-type
:   BSTR

 The name of the desired element or an asterisk (\*) to match all elements with the specified namespace.

## Return Value

Returns an object of type DOM NodeDOM Node

An IHTMLElementCollection of elements within the namespace.
