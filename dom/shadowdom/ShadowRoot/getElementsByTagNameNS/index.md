---
title: getElementsByTagNameNS
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
summary: 'Just like document.getElementsByTagNameNS except that it only works within the scope of this ShadowRoot''s shadow tree.'
uri: dom/shadowdom/ShadowRoot/getElementsByTagNameNS

---
# getElementsByTagNameNS

## Summary

Just like document.getElementsByTagNameNS except that it only works within the scope of this ShadowRoot's shadow tree.

*Method of [dom/shadowdom/ShadowRoot](/dom/shadowdom/ShadowRoot)*

## Syntax

``` {.js}
var result = element.getElementsByTagNameNS(pvarNS, bstrLocalName);
```

## Parameters

### pvarNS

 Data-typeÂ
:   VARIANT

 The namespace URI that defines the desired elements or an asterisk (\*) to match all namespaces with the document.

### bstrLocalName

 Data-typeÂ
:   BSTR

 The name of the desired element or an asterisk (\*) to match all elements with the specified namespace.

## Return Value

Returns an object of type DOM Node.

An IHTMLElementCollection of elements within the namespace.

**Needs Examples**: This section should include examples.

