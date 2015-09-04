---
title: data
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'In Progress'
standardization_status: 'W3C Working Draft'
notes:
  - 'example, standards, compatibility'
summary: 'Gets the content of the message.'
uri: dom/MessageEvent/data

---
# data

## Summary

Gets the content of the message.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/MessageEvent](/dom/MessageEvent)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var data = event.data;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">any</span></span>

The content of the message.

**Needs Examples**: This section should include examples.

## Notes

This property contains the value passed to [**postMessage**](/dom/Window/postMessage). Before trusting the data, check the [**URL**](/dom/Window/URL) property of the message request to determine its source.

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

