---
title: readyState
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
  return:
    predicate: 'Returns an object of type '
    value: enum
    href: /apis/indexeddb/IDBRequest
summary: 'The state of the request. Every request starts in the pending state. The state changes to done when the request completes successfully or when an error occurs.'
tags:
  0: API
  1: Object
  2: Properties
  4: IndexedDB
uri: apis/indexeddb/IDBRequest/readyState

---
## <span>Summary</span>

The state of the request. Every request starts in the pending state. The state changes to done when the request completes successfully or when an error occurs.

Property of [apis/indexeddb/IDBRequest](/apis/indexeddb/IDBRequest)[apis/indexeddb/IDBRequest](/apis/indexeddb/IDBRequest)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = element.readyState;
```

## <span>Return Value</span>

Returns an object of type enumenum

-   pending (1) - The request has been started, but its result is not yet available.
-   done (2) - The request has completed or an error has occurred. Initially false.

**Needs Examples**: This section should include examples.

### <span>Syntax</span>

### <span>Standards information</span>

-   [Indexed Database API](http://go.microsoft.com/fwlink/p/?LinkId=224519)
