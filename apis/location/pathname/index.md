---
title: window.location.pathname
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/location
    href: /apis/location
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /apis/location
standardization_status: 'W3C Working Draft'
summary: 'The path to the current document, relative to the root of the current host.'
tags:
  - API
  - Object
  - Properties
  - JavaScript
uri: apis/location/pathname

---
## <span>Summary</span>

The path to the current document, relative to the root of the current host.

Property of [apis/location](/apis/location)[apis/location](/apis/location)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = window.location.pathname;
```

## <span>Return Value</span>

Returns an object of type StringString

The path to the current document, relative to the root of the current host.

For example, `http://example.org/myyfolder/mypage.html` would return the pathname of `/myfoler/mypage.html`.

## <span>Examples</span>

``` js
// Returns the pathname part of the current window location.
// For this page, for instance, this will return the string '/wiki/apis/location/pathname'.
var pname = window.location.pathname;
```

## <span>Related specifications</span>

[Window Object 1.0](http://www.w3.org/TR/Window/)
:   W3C Working Draft
