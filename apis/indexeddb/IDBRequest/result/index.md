---
title: result
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/IndexedDB/IDBRequest)'
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs example, spec reference, standardization status'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/indexeddb/IDBRequest
    href: /apis/indexeddb/IDBRequest
summary: 'Returns the result of the request. If the the request failed and the result is not available, the DOMException InvalidStateError exception is thrown.'
tags:
  0: API
  1: Object
  2: Properties
  4: IndexedDB
uri: apis/indexeddb/IDBRequest/result

---
## <span>Summary</span>

Returns the result of the request. If the the request failed and the result is not available, the DOMException InvalidStateError exception is thrown.

Property of [apis/indexeddb/IDBRequest](/apis/indexeddb/IDBRequest)[apis/indexeddb/IDBRequest](/apis/indexeddb/IDBRequest)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = element.result;
```

**Needs Examples**: This section should include examples.

## <span>Notes</span>

### <span>Remarks</span>

The value of that **result** property depends on the original request. For example, if the original request opened a database, the value of the **result** property would be an [**IDBDatabase**](/apis/indexeddb/IDBDatabase) object.

### <span>Syntax</span>

### <span>Standards information</span>

-   [Indexed Database API](http://go.microsoft.com/fwlink/p/?LinkId=224519)
