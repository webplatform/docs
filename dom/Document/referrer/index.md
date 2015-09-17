---
title: 'referrer'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs examples and compat tables'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Document
    href: /dom/Document
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /dom/Document
standardization_status: 'W3C Recommendation'
summary: 'Gets the URL of the location that referred the user to the current document.'
tags:
  - API_Object_Properties
  - DOM
  - Needs_Examples
uri: dom/Document/referrer

---
## Summary

Gets the URL of the location that referred the user to the current document.

Property of [dom/Document](/dom/Document)[dom/Document](/dom/Document)

## Syntax

**Note**: This property is read-only.

``` js
var referrerURL = document.referrer;
```

## Return Value

Returns an object of type StringString

The URL of the referring document, or an empty string.

## Notes

-   It returns a value only when the user reaches the current document through a link from the previous document. Otherwise, it returns an empty string.

For example, if DocumentA.htm includes a link to DocumentB.htm, and the user clicks that link, the `document`.**referrer** on DocumentB.htm returns "DocumentA.htm." However, if the user is on DocumentA.htm and types DocumentB.htm into the address line or using some kind of "Open" method of the browser to get to DocumentB.htm, it returns the empty string.

-   It also returns an empty string when the link is from a secure site.

## Related specifications

[DOM Level 2 HTML](http://www.w3.org/TR/2003/REC-DOM-Level-2-HTML-20030109/)
:   Recommendation
