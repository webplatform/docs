---
title: 'pathname'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'compatibility, examples, standards'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Location
    href: /dom/Location
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /dom/Location
summary: 'Sets or retrieves the file name or path specified by the object.'
tags:
  - API_Object_Properties
  - DOM
  - Needs_Examples
uri: dom/Location/pathname

---
## Summary

Sets or retrieves the file name or path specified by the object.

Property of [dom/Location](/dom/Location)[dom/Location](/dom/Location)

## Syntax

``` js
var pathName = location.pathname;
location.pathname = pathName;
```

## Return Value

Returns an object of type StringString

The path component of the URL.

