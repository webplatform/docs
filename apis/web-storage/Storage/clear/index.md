---
title: clear
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/web-storage/Storage
    href: /apis/web-storage/Storage
standardization_status: 'W3C Editor''s Draft'
summary: 'Causes the list associated with the object to be emptied of all key/value pairs, if there are any.'
tags:
  - API
  - Object
  - Methods
  - Webstorage
uri: apis/web-storage/Storage/clear

---
## Summary

Causes the list associated with the object to be emptied of all key/value pairs, if there are any.

Method of [apis/web-storage/Storage](/apis/web-storage/Storage)[apis/web-storage/Storage](/apis/web-storage/Storage)

## Syntax

``` js
 object.clear();
```

## Return Value

No return value

## Examples

The following button clears the local storage area for the current domain.

``` html
<button onclick="localStorage.clear()">
    Clear Stored Values</button>
```

## Notes

sessionStorage is cleared immediately. localStorage key/value pairs are removed from memory, and disk storage quota is updated.

## Related specifications

[W3C Web Storage Specification](http://dev.w3.org/html5/webstorage)
:   W3C Editor's Draft
