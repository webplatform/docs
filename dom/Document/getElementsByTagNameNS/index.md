---
title: 'getElementsByTagNameNS'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs example and compat tables'
readiness: 'In Progress'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Document
    href: /dom/Document
  return_type:
    predicate: 'Returns an object of type  '
    value: Object
    href: /dom/Document
standardization_status: 'W3C Recommendation'
summary: 'Returns an HTMLCollection of the elements with the specified tag name and namespace.'
tags:
  - API_Object_Methods
  - DOM
  - Needs_Examples
uri: dom/Document/getElementsByTagNameNS

---
## Summary

Returns an HTMLCollection of the elements with the specified tag name and namespace.

Method of [dom/Document](/dom/Document)[dom/Document](/dom/Document)

## Syntax

``` js
var elements = document.getElementsByTagNameNS(namespace, localName);
```

## Parameters

### namespace

 Data-type
:   String

 The namespace URI that defines the desired elements or an asterisk (\*) to match all namespaces with the document, or null.

### localName

 Data-type
:   String

 The name of the desired element or an asterisk (\*) to match all elements with the specified namespace.

## Return Value

Returns an object of type ObjectObject

A live HTMLCollection of elements.

## Usage

     This method should not be used. For a more performant alternative, see the notes.

Use this method to get a live list of elements with a specified name and namespace.

## Notes

-   For performance reasons, [**querySelectorAll**](/css/selectors_api/querySelectorAll) is preferred, because it gets a static list.
-   This method returns a live element list that gets updated whenever an element is added or removed from the document, this has performance implications and may result in unexpected errors (removing elements within a for loop while caching the length of the collection).
-   If namespaces are irrelevant in the context, [getElementsByTagName](/dom/Document/getElementsByTagName) can be used (but it is also not recommended; see the first two notes).

## Related specifications

[DOM](http://dom.spec.whatwg.org/)
:   Living Standard

[DOM Level 4](http://www.w3.org/TR/2014/CR-dom-20140508/#dom-document-getelementsbytagnamens)
:   Candidate Recommendation

[Document Object Model (DOM) Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation

[Document Object Model (DOM) Level 2 Core](http://www.w3.org/TR/DOM-Level-2-Core/)
:   Recommendation
