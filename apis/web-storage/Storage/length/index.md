---
title: length
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/web-storage/Storage
    href: /apis/web-storage/Storage
  return:
    predicate: 'Returns an object of type '
    value: 'unsigned long'
    href: /apis/web-storage/Storage
standardization_status: 'W3C Editor''s Draft'
summary: 'Returns the number of key/value pairs currently present in the list associated with the object.'
tags:
  - API
  - Object
  - Properties
  - Webstorage
uri: apis/web-storage/Storage/length

---
## <span>Summary</span>

Returns the number of key/value pairs currently present in the list associated with the object.

Property of [apis/web-storage/Storage](/apis/web-storage/Storage)[apis/web-storage/Storage](/apis/web-storage/Storage)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = object.length;
```

## <span>Return Value</span>

Returns an object of type unsigned longunsigned long

## <span>Examples</span>

This example creates two new localStorage items (a timestamp and a user name), then reports the number of key/value pairs (2).

``` js
window.localStorage.setItem('timestamp', (new Date()).getTime());
window.localStorage.setItem('user', 'Bob');
alert("There are " + window.localStorage.length + " localStorage item(s)");
```

## <span>Related specifications</span>

[W3C Web Storage Specification](http://dev.w3.org/html5/webstorage)
:   W3C Editor's Draft
