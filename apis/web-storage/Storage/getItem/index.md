---
title: getItem
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/web-storage/Storage
    href: /apis/web-storage/Storage
  return_type:
    predicate: 'Returns an object of type  '
    value: String
    href: /apis/web-storage/Storage
standardization_status: 'W3C Editor''s Draft'
summary: 'Returns the current value associated with the given key.'
tags:
  - API
  - Object
  - Methods
  - Webstorage
uri: apis/web-storage/Storage/getItem

---
## <span>Summary</span>

Returns the current value associated with the given key.

Method of [apis/web-storage/Storage](/apis/web-storage/Storage)[apis/web-storage/Storage](/apis/web-storage/Storage)

## <span>Syntax</span>

``` js
var  = object.getItem(key);
```

## <span>Parameters</span>

### <span>key</span>

 Data-type
:   String

 The name of the key (a valid UTF-16 string, including the empty string).

## <span>Return Value</span>

Returns an object of type StringString

## <span>Examples</span>

This example creates a new localStorage item (a timestamp) and sets it with a unique key, then executes a function, then retrieves the timestamp by its key and reports it.

``` js
window.localStorage.setItem('timestamp', (new Date()).getTime());
doSomethingElse();
startTime = window.localStorage.getItem('timestamp');
alert("The doSomethingElse function was called at: " + startTime);
```

## <span>Notes</span>

Any valid UTF-16 string, including the empty string, is a valid key name. If the specified *key* does not exist in the list associated with the object, then this method returns **null**. Attempts to read or write a secured item from script running in the context of an unsecured URL are not permitted.

## <span>Related specifications</span>

[W3C Web Storage Specification](http://dev.w3.org/html5/webstorage)
:   W3C Editor's Draft
