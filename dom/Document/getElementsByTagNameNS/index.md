---
title: getElementsByTagNameNS
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'In Progress'
standardization_status: 'W3C Recommendation'
notes:
  - 'Needs example and compat tables'
summary: 'Returns an HTMLCollection of the elements with the specified tag name and namespace.'
uri: dom/Document/getElementsByTagNameNS

---
# getElementsByTagNameNS

## Summary

Returns an HTMLCollection of the elements with the specified tag name and namespace.

*Method of [dom/Document](/dom/Document)*

## Syntax

``` {.js}
var elements = document.getElementsByTagNameNS(namespace, localName);
```

## Parameters

### namespace

 Data-typeÂ
:   String

 The namespace URI that defines the desired elements or an asterisk (\*) to match all namespaces with the document, or null.

### localName

 Data-typeÂ
:   String

 The name of the desired element or an asterisk (\*) to match all elements with the specified namespace.

## Return Value

Returns an object of type Object.

A live HTMLCollection of elements.

**Needs Examples**: This section should include examples.

## Usage

     This method should not be used. For a more performant alternative, see the notes.

Use this method to get a live list of elements with a specified name and namespace.

## Notes

-   For performance reasons, [**querySelectorAll**](/css/selectors_api/querySelectorAll) is preferred, because it gets a static list.
-   This method returns a live element list that gets updated whenever an element is added or removed from the document, this has performance implications and may result in unexpected errors (removing elements within a for loop while caching the length of the collection).
-   If namespaces are irrelevant in the context, [getElementsByTagName](/dom/Document/getElementsByTagName) can be used (but it is also not recommended; see the first two notes).

## Related specifications

Specification
:   Status
[DOM](http://dom.spec.whatwg.org/)
:   Living Standard
[DOM Level 4](http://www.w3.org/TR/2014/CR-dom-20140508/#dom-document-getelementsbytagnamens)
:   Candidate Recommendation
[Document Object Model (DOM) Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation
[Document Object Model (DOM) Level 2 Core](http://www.w3.org/TR/DOM-Level-2-Core/)
:   Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

