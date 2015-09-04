---
title: search
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Almost Ready'
notes:
  - 'compatibility, standards'
summary: 'Sets or retrieves the substring of the href property that follows the question mark.'
uri: dom/Location/search

---
# search

## Summary

Sets or retrieves the substring of the href property that follows the question mark.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Location](/dom/Location)</span></span>

## Syntax

``` {.js}
var queryString = location.search;
location.search = queryString;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

The query string component of the URL.

## Examples

This example function returns the **search** property of the current page location.

``` {.js}
function getSearch() {
    return document.location.search;
}
```

## Notes

The substring that follows the question mark is the query string or form data.

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

