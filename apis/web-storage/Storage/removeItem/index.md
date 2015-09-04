---
title: removeItem
tags:
  - API
  - Object
  - Methods
  - Webstorage
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Removes the key/value pair with the given key from the list associated with the object, if it exists.'
uri: apis/web-storage/Storage/removeItem

---
# removeItem

## Summary

Removes the key/value pair with the given key from the list associated with the object, if it exists.

*Method of [apis/web-storage/Storage](/apis/web-storage/Storage)*

## Syntax

``` {.js}
 object.removeItem(key);
```

## Parameters

### key

 Data-typeÂ
:   String

 The name of the key, or the empty string.

## Return Value

No return value

## Examples

``` {.js}
// Check for support of sessionStorage
if(window.sessionStorage) {

  // Add a key/value pair
  sessionStorage.setItem('someKey', 'value');

  // Remove the item you just added
  sessionStorage.removeItem('someKey');
}
```

## Related specifications

Specification
:   Status
[W3C Web Storage Specification](http://dev.w3.org/html5/webstorage)
:   W3C Editor's Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

