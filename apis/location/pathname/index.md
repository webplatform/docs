---
title: pathname
tags:
  - API
  - Object
  - Properties
  - JavaScript
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'The path to the current document, relative to the root of the current host.'
uri: apis/location/pathname

---
# window.location.pathname

## Summary

The path to the current document, relative to the root of the current host.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/location](/apis/location)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = window.location.pathname;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

The path to the current document, relative to the root of the current host.

For example, `http://example.org/myyfolder/mypage.html` would return the pathname of `/myfoler/mypage.html`.

## Examples

``` {.js}
// Returns the pathname part of the current window location.
// For this page, for instance, this will return the string '/wiki/apis/location/pathname'.
var pname = window.location.pathname;
```

## Related specifications

Specification
:   Status
[Window Object 1.0](http://www.w3.org/TR/Window/)
:   W3C Working Draft

