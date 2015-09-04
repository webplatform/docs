---
title: referrer
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'In Progress'
standardization_status: 'W3C Recommendation'
notes:
  - 'Needs examples and compat tables'
summary: 'Gets the URL of the location that referred the user to the current document.'
uri: dom/Document/referrer

---
# referrer

## Summary

Gets the URL of the location that referred the user to the current document.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Document](/dom/Document)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var referrerURL = document.referrer;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

The URL of the referring document, or an empty string.

**Needs Examples**: This section should include examples.

## Notes

-   It returns a value only when the user reaches the current document through a link from the previous document. Otherwise, it returns an empty string.

For example, if DocumentA.htm includes a link to DocumentB.htm, and the user clicks that link, the `document`.**referrer** on DocumentB.htm returns "DocumentA.htm." However, if the user is on DocumentA.htm and types DocumentB.htm into the address line or using some kind of "Open" method of the browser to get to DocumentB.htm, it returns the empty string.

-   It also returns an empty string when the link is from a secure site.

## Related specifications

Specification
:   Status
[DOM Level 2 HTML](http://www.w3.org/TR/2003/REC-DOM-Level-2-HTML-20030109/)
:   Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

