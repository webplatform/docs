---
title: origin
tags:
  - API
  - Object
  - Properties
  - DOM
  - DOMEvents
readiness: 'Almost Ready'
standardization_status: 'W3C Working Draft'
notes:
  - 'examples, compatibility'
summary: 'Gets the URL of the document of origin.'
uri: dom/MessageEvent/origin

---
# origin

## Summary

Gets the URL of the document of origin.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/MessageEvent](/dom/MessageEvent)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var messageOrigin = event.origin;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

The origin URL of the document that sent the message.

**Needs Examples**: This section should include examples.

## Notes

In cross-document messaging, this property represents the originating URI of the document that sent the message (typically the URI includes the scheme, host name, and port of the document, but not its path or fragment identifier).

## Related specifications

Specification
:   Status
[W3C HTML5](http://www.w3.org/TR/html5/)
:   Working Draft
[WHATWG HTML](http://www.whatwg.org/specs/web-apps/current-work/multipage)
:   Living Standard

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

