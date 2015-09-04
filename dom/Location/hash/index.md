---
title: hash
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Almost Ready'
notes:
  - 'More description, compatibility'
summary: 'Sets or retrieves the subsection of the href property that follows the number sign (#).'
uri: dom/Location/hash

---
# hash

## Summary

Sets or retrieves the subsection of the href property that follows the number sign (\#).

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Location](/dom/Location)</span></span>

## Syntax

``` {.js}
var hash = location.hash;
location.hash = hash;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

The hash component of the URL.

## Examples

This example function returns true if the current document URL has a **hash** value, or false if the document URL does not.

``` {.js}
function hasHash() {
    if (document.location.hash === "") {
        return false;
    }
    return true;
}
```

## Notes

If there is no number sign, this property returns an empty string. This property is useful for moving to a bookmark within a document. Assigning an invalid value does not cause an error.

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

