---
title: reload
tags:
  - API
  - Object
  - Methods
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Refresh/reload the current page, optionally forcing a re-download of the content.'
uri: apis/location/reload

---
# window.location.reload

## Summary

Refresh/reload the current page, optionally forcing a re-download of the content.

*Method of [apis/location](/apis/location)*

## Syntax

``` {.js}
var  = window.location.reload(forceget);
```

## Parameters

### forceget

 Data-typeÂ
:   String

 Boolean, true forces a download the page contents again.

## Return Value

Returns an object of type .

## Examples

``` {.js}
//force the page to reload/refresh
window.location.reload();
```

## Related specifications

Specification
:   Status
[Window Object 1.0](http://www.w3.org/TR/Window/)
:   W3C Working Draft

