---
title: source
tags:
  - API
  - Object
  - Properties
  - DOM
  - DOMEvents
readiness: 'Almost Ready'
standardization_status: 'W3C Working Draft'
notes:
  - 'example, compatibility'
summary: 'Gets the window object that sent the message.'
uri: dom/MessageEvent/source

---
# source

## Summary

Gets the window object that sent the message.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/MessageEvent](/dom/MessageEvent)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var sourceWindow = event.source;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Object</span></span>

The window that sent the message.

**Needs Examples**: This section should include examples.

## Notes

In cross-document messaging, this property provides access to the **window** object that sent the message.

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

