---
title: window.location.assign
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/location
    href: /apis/location
  return_type:
    predicate: 'Returns an object of type  '
    value: ''
    href: /apis/location
standardization_status: 'W3C Editor''s Draft'
summary: 'Navigate to a new page.'
tags:
  - API
  - Object
  - Methods
  - JavaScript
uri: apis/location/assign

---
## Summary

Navigate to a new page.

Method of [apis/location](/apis/location)[apis/location](/apis/location)

## Syntax

``` js
var  = window.location.assign(url);
```

## Parameters

### url

 Data-type
:   String

 The new URL to navigate to.

## Return Value

Returns an object of type

## Examples

Navigate to example.org.

``` js
window.location.assign("http://example.org/");
```

The `assign` method is synonymous with replacing the `window.location` object with a string.

``` js
window.location = "http://example.org/";
```

## Related specifications

[Window Object 1.0](http://www.w3.org/TR/Window/)
:   W3C Working Draft
