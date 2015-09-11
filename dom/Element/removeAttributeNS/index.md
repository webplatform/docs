---
title: removeAttributeNS
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs examples and compat'
readiness: 'Almost Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Element
    href: /dom/Element
standardization_status: 'W3C Recommendation'
summary: 'Removes a specified content attribute in a specified namespace from an element.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Element/removeAttributeNS

---
## <span>Summary</span>

Removes a specified content attribute in a specified namespace from an element.

Method of [dom/Element](/dom/Element)[dom/Element](/dom/Element)

## <span>Syntax</span>

``` js
 element.removeAttributeNS(namespaceURI, name);
```

## <span>Parameters</span>

### <span>namespaceURI</span>

 Data-type
:   String

 The namespace name of the attribute to remove.

### <span>name</span>

 Data-type
:   String

 The local name of the attribute to remove.

## <span>Return Value</span>

No return value

**Needs Examples**: This section should include examples.

## <span>Usage</span>

     Use this method to remove a content attribute in a specified namespace from an element.

## <span>Notes</span>

-   The attribute to remove may not exist in the first place.
-   Where namespaces are irrelevant, [removeAttribute](/dom/Element/removeAttribute) can be used instead.

## <span>Related specifications</span>

[Document Object Model (DOM) Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation

[Document Object Model (DOM) Level 2 Core](http://www.w3.org/TR/DOM-Level-2-Core/)
:   Recommendation

[DOM](http://dom.spec.whatwg.org/)
:   Living Standard
