---
title: 'hash'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'More description, compatibility'
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
summary: 'Sets or retrieves the subsection of the href property that follows the number sign (#).'
tags:
  - API_Object_Properties
  - DOM
uri: dom/Location/hash

---
## Summary

Sets or retrieves the subsection of the href property that follows the number sign (\#).

Property of [dom/Location](/dom/Location)[dom/Location](/dom/Location)

## Syntax

``` js
var hash = location.hash;
location.hash = hash;
```

## Return Value

Returns an object of type StringString

The hash component of the URL.

## Examples

This example function returns true if the current document URL has a **hash** value, or false if the document URL does not.

``` js
function hasHash() {
    if (document.location.hash === "") {
        return false;
    }
    return true;
}
```

## Notes

If there is no number sign, this property returns an empty string. This property is useful for moving to a bookmark within a document. Assigning an invalid value does not cause an error.
