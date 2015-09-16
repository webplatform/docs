---
title: 'window.location.reload'
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
standardization_status: 'W3C Working Draft'
summary: 'Refresh/reload the current page, optionally forcing a re-download of the content.'
tags:
  - API
  - Object
  - Methods
uri: apis/location/reload

---
## Summary

Refresh/reload the current page, optionally forcing a re-download of the content.

Method of [apis/location](/apis/location)[apis/location](/apis/location)

## Syntax

``` js
var  = window.location.reload(forceget);
```

## Parameters

### forceget

 Data-type
:   String

 Boolean, true forces a download the page contents again.

## Return Value

Returns an object of type

## Examples

``` js
//force the page to reload/refresh
window.location.reload();
```

## Related specifications

[Window Object 1.0](http://www.w3.org/TR/Window/)
:   W3C Working Draft

