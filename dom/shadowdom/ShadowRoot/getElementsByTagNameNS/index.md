---
title: getElementsByTagNameNS
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
  - API
  - Object
  - Methods
  - DOM
  - Shadow
uri: dom/shadowdom/ShadowRoot/getElementsByTagNameNS

---
## <span>Summary</span>

Just like document.getElementsByTagNameNS except that it only works within the scope of this ShadowRoot's shadow tree.

Method of [dom/shadowdom/ShadowRoot](/dom/shadowdom/ShadowRoot)[dom/shadowdom/ShadowRoot](/dom/shadowdom/ShadowRoot)

## <span>Syntax</span>

``` js
var result = element.getElementsByTagNameNS(pvarNS, bstrLocalName);
```

## <span>Parameters</span>

### <span>pvarNS</span>

 Data-type
:   VARIANT

 The namespace URI that defines the desired elements or an asterisk (\*) to match all namespaces with the document.

### <span>bstrLocalName</span>

 Data-type
:   BSTR

 The name of the desired element or an asterisk (\*) to match all elements with the specified namespace.

## <span>Return Value</span>

Returns an object of type DOM NodeDOM Node

An IHTMLElementCollection of elements within the namespace.

**Needs Examples**: This section should include examples.

