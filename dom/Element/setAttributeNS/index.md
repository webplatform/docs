---
title: setAttributeNS
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs examples and compat'
readiness: 'In Progress'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Element
    href: /dom/Element
standardization_status: 'W3C Recommendation'
summary: 'Sets the value of a content attribute in a specified namespace.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Element/setAttributeNS

---
## <span>Summary</span>

Sets the value of a content attribute in a specified namespace.

Method of [dom/Element](/dom/Element)[dom/Element](/dom/Element)

## <span>Syntax</span>

``` js
 element.setAttributeNS(namespaceURI, name, value);
```

## <span>Parameters</span>

### <span>namespaceURI</span>

 Data-type
:   String

 The namespace URI of the attribute, or null.

### <span>name</span>

 Data-type
:   String

 The local name of the attribute within the specified namespace.

### <span>value</span>

 Data-type
:   String

 The value of the attribute.

## <span>Return Value</span>

No return value

**Needs Examples**: This section should include examples.

## <span>Usage</span>

     Use this method to set an attribute in a specified namespace.

## <span>Notes</span>

-   The attribute will be created, if it is not already present.
-   Where namespaces are irrelevant, [setAttribute](/dom/Element/setAttribute) can be used instead.

## <span>Related specifications</span>

[Document Object Model (DOM) Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation

[Document Object Model (DOM) Level 2 Core](http://www.w3.org/TR/DOM-Level-2-Core/)
:   Recommendation

[DOM](http://dom.spec.whatwg.org/)
:   Living Standard
