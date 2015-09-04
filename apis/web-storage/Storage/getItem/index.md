---
title: getItem
tags:
  - API
  - Object
  - Methods
  - Webstorage
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Returns the current value associated with the given key.'
uri: apis/web-storage/Storage/getItem

---
# getItem

## Summary

Returns the current value associated with the given key.

*Method of [apis/web-storage/Storage](/apis/web-storage/Storage)*

## Syntax

``` {.js}
var  = object.getItem(key);
```

## Parameters

### key

 Data-typeÂ
:   String

 The name of the key (a valid UTF-16 string, including the empty string).

## Return Value

Returns an object of type String.

## Examples

This example creates a new localStorage item (a timestamp) and sets it with a unique key, then executes a function, then retrieves the timestamp by its key and reports it.

``` {.js}
window.localStorage.setItem('timestamp', (new Date()).getTime());
doSomethingElse();
startTime = window.localStorage.getItem('timestamp');
alert("The doSomethingElse function was called at: " + startTime);
```

## Notes

Any valid UTF-16 string, including the empty string, is a valid key name. If the specified *key* does not exist in the list associated with the object, then this method returns **null**. Attempts to read or write a secured item from script running in the context of an unsecured URL are not permitted.

## Related specifications

Specification
:   Status
[W3C Web Storage Specification](http://dev.w3.org/html5/webstorage)
:   W3C Editor's Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

