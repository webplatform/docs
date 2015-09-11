---
title: error
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/IndexedDB/IDBTransaction)'
notes:
  - 'Needs example, spec reference'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/indexeddb/IDBTransaction
    href: /apis/indexeddb/IDBTransaction
  return:
    predicate: 'Returns an object of type '
    value: DOMError
    href: /apis/indexeddb/IDBTransaction
standardization_status: 'W3C Proposed Recommendation'
summary: 'Null if the transaction is not finished, is finished and successfully committed, or was aborted with the abort() function. Returns the same DOMError as the request object which caused the transaction to be aborted due to a failed request, or a DOMError for the transaction failure not due to a failed request (such as QuotaExceededError or UnknownError).'
tags:
  0: API
  1: Object
  2: Properties
  4: IndexedDB
uri: apis/indexeddb/IDBTransaction/error

---
## <span>Summary</span>

Null if the transaction is not finished, is finished and successfully committed, or was aborted with the abort() function. Returns the same DOMError as the request object which caused the transaction to be aborted due to a failed request, or a DOMError for the transaction failure not due to a failed request (such as QuotaExceededError or UnknownError).

Property of [apis/indexeddb/IDBTransaction](/apis/indexeddb/IDBTransaction)[apis/indexeddb/IDBTransaction](/apis/indexeddb/IDBTransaction)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = element.error;
```

## <span>Return Value</span>

Returns an object of type DOMErrorDOMError

**Needs Examples**: This section should include examples.

