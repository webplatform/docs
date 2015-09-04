---
title: error
tags:
  0: API
  1: Object
  2: Properties
  4: IndexedDB
readiness: 'In Progress'
standardization_status: 'W3C Proposed Recommendation'
notes:
  - 'Needs example, spec reference'
summary: 'Null if the transaction is not finished, is finished and successfully committed, or was aborted with the abort() function. Returns the same DOMError as the request object which caused the transaction to be aborted due to a failed request, or a DOMError for the transaction failure not due to a failed request (such as QuotaExceededError or UnknownError).'
uri: apis/indexeddb/IDBTransaction/error

---
# error

## Summary

Null if the transaction is not finished, is finished and successfully committed, or was aborted with the abort() function. Returns the same DOMError as the request object which caused the transaction to be aborted due to a failed request, or a DOMError for the transaction failure not due to a failed request (such as QuotaExceededError or UnknownError).

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/indexeddb/IDBTransaction](/apis/indexeddb/IDBTransaction)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = element.error;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">DOMError</span></span>

**Needs Examples**: This section should include examples.

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/IndexedDB/IDBTransaction)

