---
title: setAttributeNS
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'In Progress'
standardization_status: 'W3C Recommendation'
notes:
  - 'Needs examples and compat'
summary: 'Sets the value of a content attribute in a specified namespace.'
uri: dom/Element/setAttributeNS

---
# setAttributeNS

## Summary

Sets the value of a content attribute in a specified namespace.

*Method of [dom/Element](/dom/Element)*

## Syntax

``` {.js}
 element.setAttributeNS(namespaceURI, name, value);
```

## Parameters

### namespaceURI

 Data-typeÂ
:   String

 The namespace URI of the attribute, or null.

### name

 Data-typeÂ
:   String

 The local name of the attribute within the specified namespace.

### value

 Data-typeÂ
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

Specification
:   Status
[Document Object Model (DOM) Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation
[Document Object Model (DOM) Level 2 Core](http://www.w3.org/TR/DOM-Level-2-Core/)
:   Recommendation
[DOM](http://dom.spec.whatwg.org/)
:   Living Standard

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

