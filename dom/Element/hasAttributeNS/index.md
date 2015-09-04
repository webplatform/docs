---
title: hasAttributeNS
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'In Progress'
standardization_status: 'W3C Recommendation'
notes:
  - 'Needs example and compat table'
summary: 'Determines whether a content attribute in a specified namespace exists on an element.'
uri: dom/Element/hasAttributeNS

---
# hasAttributeNS

## Summary

Determines whether a content attribute in a specified namespace exists on an element.

*Method of [dom/Element](/dom/Element)*

## Syntax

``` {.js}
var attributeExists = element.hasAttributeNS(namespaceURI, name);
```

## Parameters

### namespaceURI

 Data-typeÂ
:   String

 The namespace URI that defines the attribute name, or null.

### name

 Data-typeÂ
:   String

 The name of the attribute.

## Return Value

Returns an object of type Boolean.

Whether the specified attribute exists.

**Needs Examples**: This section should include examples.

## Usage

     Use this method to determine whether a content attribute in a specified namespace exists on an element.

## Notes

-   This method does not get the value of the attribute, see [getAttributeNS](/dom/Element/getAttributeNS) for this purpose.
-   Where namespaces are irrelevant, [hasAttribute](/dom/Element/hasAttribute) can be used instead.
-   See [hasAttributes](/dom/Node/hasAttributes), which determines whether the element has any attributes at all.

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

