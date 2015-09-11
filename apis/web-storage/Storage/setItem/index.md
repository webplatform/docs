---
title: setItem
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/web-storage/Storage
    href: /apis/web-storage/Storage
standardization_status: 'W3C Editor''s Draft'
summary: 'Adds or replaces a value for the given key.'
tags:
  - API
  - Object
  - Methods
  - Webstorage
uri: apis/web-storage/Storage/setItem

---
## <span>Summary</span>

Adds or replaces a value for the given key.

Method of [apis/web-storage/Storage](/apis/web-storage/Storage)[apis/web-storage/Storage](/apis/web-storage/Storage)

## <span>Syntax</span>

``` js
 object.setItem(key, value);
```

## <span>Parameters</span>

### <span>key</span>

 Data-type
:   String

 The name of the key (a valid UTF-16 string, including the empty string).

### <span>value</span>

 Data-type
:   String

 The value (a valid UTF-16 string) for the key/value pair.

## <span>Return Value</span>

No return value

## <span>Examples</span>

The following code examples are equivalent. The first sets a key/value pair by calling **setItem**. The second uses array syntax to find the key in the collection. The final example uses property name syntax to set an expando property.

``` js
sessionStorage.setItem('myKey', '...');

sessionStorage['myKey'] = '...';

sessionStorage.myKey = '...';
```

## <span>Notes</span>

Any valid UTF-16 string, including the empty string, is a valid key name. If *key* or *value* are not valid UTF-16 strings, the **setItem** method throws an error. Non-string variable types are automatically type-converted to strings, if possible. Structured data must be converted to a string before storing. This method first checks if a key/value pair with the specified *key* already exists in the list associated with the object. If not, a new key/value pair with the given value is added to the list. If the key/value pair already exists, the value is updated. Keys are also available as expando properties on the **Storage** object. If the property name does not exist, a key/value pair is created for it. If the size of the value is larger than the disk quota remaining for the storage area, an "Out of memory" exception is thrown. Attempts to read or write a secured item from script running in the context of an unsecured URL are not permitted.

## <span>Related specifications</span>

[W3C Web Storage Specification](http://dev.w3.org/html5/webstorage)
:   W3C Editor's Draft
