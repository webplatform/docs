---
title: removeItem
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/web-storage/Storage
    href: /apis/web-storage/Storage
standardization_status: 'W3C Editor''s Draft'
summary: 'Removes the key/value pair with the given key from the list associated with the object, if it exists.'
tags:
  - API
  - Object
  - Methods
  - Webstorage
uri: apis/web-storage/Storage/removeItem

---
## <span>Summary</span>

Removes the key/value pair with the given key from the list associated with the object, if it exists.

Method of [apis/web-storage/Storage](/apis/web-storage/Storage)[apis/web-storage/Storage](/apis/web-storage/Storage)

## <span>Syntax</span>

``` js
 object.removeItem(key);
```

## <span>Parameters</span>

### <span>key</span>

 Data-type
:   String

 The name of the key, or the empty string.

## <span>Return Value</span>

No return value

## <span>Examples</span>

``` js
// Check for support of sessionStorage
if(window.sessionStorage) {

  // Add a key/value pair
  sessionStorage.setItem('someKey', 'value');

  // Remove the item you just added
  sessionStorage.removeItem('someKey');
}
```

## <span>Related specifications</span>

[W3C Web Storage Specification](http://dev.w3.org/html5/webstorage)
:   W3C Editor's Draft
