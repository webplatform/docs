---
title: length
tags:
  - API
  - Object
  - Properties
  - Webstorage
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Returns the number of key/value pairs currently present in the list associated with the object.'
uri: apis/web-storage/Storage/length

---
# length

## Summary

Returns the number of key/value pairs currently present in the list associated with the object.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/web-storage/Storage](/apis/web-storage/Storage)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = object.length;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">unsigned long</span></span>

## Examples

This example creates two new localStorage items (a timestamp and a user name), then reports the number of key/value pairs (2).

``` {.js}
window.localStorage.setItem('timestamp', (new Date()).getTime());
window.localStorage.setItem('user', 'Bob');
alert("There are " + window.localStorage.length + " localStorage item(s)");
```

## Related specifications

Specification
:   Status
[W3C Web Storage Specification](http://dev.w3.org/html5/webstorage)
:   W3C Editor's Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

