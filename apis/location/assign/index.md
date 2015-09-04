---
title: assign
tags:
  - API
  - Object
  - Methods
  - JavaScript
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Navigate to a new page.'
uri: apis/location/assign

---
# window.location.assign

## Summary

Navigate to a new page.

*Method of [apis/location](/apis/location)*

## Syntax

``` {.js}
var  = window.location.assign(url);
```

## Parameters

### url

 Data-typeÂ
:   String

 The new URL to navigate to.

## Return Value

Returns an object of type .

## Examples

Navigate to example.org.

``` {.js}
window.location.assign("http://example.org/");
```

The `assign` method is synonymous with replacing the `window.location` object with a string.

``` {.js}
window.location = "http://example.org/";
```

## Related specifications

Specification
:   Status
[Window Object 1.0](http://www.w3.org/TR/Window/)
:   W3C Working Draft

