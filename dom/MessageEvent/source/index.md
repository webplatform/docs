---
title: 'source'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'example, compatibility'
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/MessageEvent
    href: /dom/MessageEvent
  return:
    predicate: 'Returns an object of type '
    value: Object
    href: /dom/MessageEvent
standardization_status: 'W3C Working Draft'
summary: 'Gets the window object that sent the message.'
tags:
  - API_Object_Properties
  - DOM
  - DOMEvents
  - Needs_Examples
uri: dom/MessageEvent/source

---
## Summary

Gets the window object that sent the message.

Property of [dom/MessageEvent](/dom/MessageEvent)[dom/MessageEvent](/dom/MessageEvent)

## Syntax

**Note**: This property is read-only.

``` js
var sourceWindow = event.source;
```

## Return Value

Returns an object of type ObjectObject

The window that sent the message.

## Notes

In cross-document messaging, this property provides access to the **window** object that sent the message.

## Related specifications

[W3C HTML5](http://www.w3.org/TR/html5/)
:   Working Draft

[WHATWG HTML](http://www.whatwg.org/specs/web-apps/current-work/multipage)
:   Living Standard
