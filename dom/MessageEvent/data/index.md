---
title: 'data'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'example, standards, compatibility'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/MessageEvent
    href: /dom/MessageEvent
  return:
    predicate: 'Returns an object of type '
    value: any
    href: /dom/MessageEvent
standardization_status: 'W3C Working Draft'
summary: 'Gets the content of the message.'
tags:
  - API_Object_Properties
  - DOM
  - Needs_Examples
uri: dom/MessageEvent/data

---
## Summary

Gets the content of the message.

Property of [dom/MessageEvent](/dom/MessageEvent)[dom/MessageEvent](/dom/MessageEvent)

## Syntax

**Note**: This property is read-only.

``` js
var data = event.html/elements/data;
```

## Return Value

Returns an object of type anyany

The content of the message.

## Notes

This property contains the value passed to [**postMessage**](/dom/Window/postMessage). Before trusting the data, check the [**URL**](/dom/Window/URL) property of the message request to determine its source.
