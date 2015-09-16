---
title: origin
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'examples, compatibility'
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/MessageEvent
    href: /dom/MessageEvent
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /dom/MessageEvent
standardization_status: 'W3C Working Draft'
summary: 'Gets the URL of the document of origin.'
tags:
  - API
  - Object
  - Properties
  - DOM
  - DOMEvents
uri: dom/MessageEvent/origin

---
## Summary

Gets the URL of the document of origin.

Property of [dom/MessageEvent](/dom/MessageEvent)[dom/MessageEvent](/dom/MessageEvent)

## Syntax

**Note**: This property is read-only.

``` js
var messageOrigin = event.origin;
```

## Return Value

Returns an object of type StringString

The origin URL of the document that sent the message.

**Needs Examples**: This section should include examples.

## Notes

In cross-document messaging, this property represents the originating URI of the document that sent the message (typically the URI includes the scheme, host name, and port of the document, but not its path or fragment identifier).

## Related specifications

[W3C HTML5](http://www.w3.org/TR/html5/)
:   Working Draft

[WHATWG HTML](http://www.whatwg.org/specs/web-apps/current-work/multipage)
:   Living Standard
