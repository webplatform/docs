---
title: key
tags:
  - API
  - Object
  - Methods
  - Webstorage
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Returns the name of the nth key in the list.'
uri: apis/web-storage/Storage/key

---
# key

## Summary

Returns the name of the nth key in the list.

*Method of [apis/web-storage/Storage](/apis/web-storage/Storage)*

## Syntax

``` {.js}
var  = object.key(index);
```

## Parameters

### index

 Data-typeÂ
:   unsigned long

 A zero-based index of the list entry, up to the length of the collection.

## Return Value

Returns an object of type String.

## Examples

This example creates a new localStorage item (a timestamp) and sets it with a unique key, then executes a function, then retrieves the item's name by its key index (0 in this case, as it is the first key) and reports its value.

``` {.js}
window.localStorage.setItem('timestamp', (new Date()).getTime());
doSomethingElse();
startTimeKey = window.localStorage.key(0);
startTime = window.localStorage.getItem(startTimeKey);
alert("The doSomethingElse function was called at: " + startTime);
```

## Notes

The returned key can be any string, including the empty string. The order of keys may change when items are added to the collection. This method will throw an "Invalid Argument" exception if *index* is out of range.

## Related specifications

Specification
:   Status
[W3C Web Storage Specification](http://dev.w3.org/html5/webstorage)
:   W3C Editor's Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

