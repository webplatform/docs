---
title: window.location.reload
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
## <span>Summary</span>

Refresh/reload the current page, optionally forcing a re-download of the content.

Method of [apis/location](/apis/location)[apis/location](/apis/location)

## <span>Syntax</span>

``` js
var  = window.location.reload(forceget);
```

## <span>Parameters</span>

### <span>forceget</span>

 Data-type
:   String

 Boolean, true forces a download the page contents again.

## <span>Return Value</span>

Returns an object of type<span></span>

## <span>Examples</span>

``` js
//force the page to reload/refresh
window.location.reload();
```

## <span>Related specifications</span>

[Window Object 1.0](http://www.w3.org/TR/Window/)
:   W3C Working Draft

