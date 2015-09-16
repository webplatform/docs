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
## Summary

Sets the value of a content attribute in a specified namespace.

Method of [dom/Element](/dom/Element)[dom/Element](/dom/Element)

## Syntax

``` js
 element.setAttributeNS(namespaceURI, name, value);
```

## Parameters

### namespaceURI

 Data-type
:   String

 The namespace URI of the attribute, or null.

### name

 Data-type
:   String

 The local name of the attribute within the specified namespace.

### value

 Data-type
:   String

 The value of the attribute.

## Return Value

No return value

**Needs Examples**: This section should include examples.

## Usage

     Use this method to set an attribute in a specified namespace.

## Notes

-   The attribute will be created, if it is not already present.
-   Where namespaces are irrelevant, [setAttribute](/dom/Element/setAttribute) can be used instead.

## Related specifications

[Document Object Model (DOM) Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation

[Document Object Model (DOM) Level 2 Core](http://www.w3.org/TR/DOM-Level-2-Core/)
:   Recommendation

[DOM](http://dom.spec.whatwg.org/)
:   Living Standard
