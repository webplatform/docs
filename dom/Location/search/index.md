---
title: 'search'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'compatibility, standards'
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Location
    href: /dom/Location
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /dom/Location
summary: 'Sets or retrieves the substring of the href property that follows the question mark.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Location/search

---
## Summary

Sets or retrieves the substring of the href property that follows the question mark.

Property of [dom/Location](/dom/Location)[dom/Location](/dom/Location)

## Syntax

``` js
var queryString = location.search;
location.search = queryString;
```

## Return Value

Returns an object of type StringString

The query string component of the URL.

## Examples

This example function returns the **search** property of the current page location.

``` js
function getSearch() {
    return document.location.search;
}
```

## Notes

The substring that follows the question mark is the query string or form data.
