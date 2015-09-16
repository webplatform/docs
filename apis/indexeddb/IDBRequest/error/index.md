---
title: 'error'
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
    value: DOMError
    href: /apis/indexeddb/IDBRequest
summary: 'The error codes returned under certain conditions.'
tags:
  0: API
  1: Object
  2: Properties
  4: IndexedDB
uri: apis/indexeddb/IDBRequest/error

---
## Summary

The error codes returned under certain conditions.

Property of [apis/indexeddb/IDBRequest](/apis/indexeddb/IDBRequest)[apis/indexeddb/IDBRequest](/apis/indexeddb/IDBRequest)

## Syntax

**Note**: This property is read-only.

``` js
var result = element.error;
```

## Return Value

Returns an object of type DOMErrorDOMError

**Needs Examples**: This section should include examples.

## Usage

     The following error codes are returned under certain conditions:

-   AbortError — If you abort the transaction, then all requests still in progress receive this error.
-   ConstraintError — If you insert data that doesn't conform to a constraint. It's an exception type for creating stores and indexes. You get this error, for example, if you try to add a new key that already exists in the record.
-   QuotaExceededError — If you run out of disk quota and the user declined to grant you more space.
-   UnknownError — If the operation failed for reasons unrelated to the database itself. A failure due to disk IO errors is such an example.
-   NoError — If the request succeeds.
-   VersionError — If you try to open a database with a version lower than the one it already has.

In addition to the error codes sent to the IDBRequest object, asynchronous operations can also raise exceptions. The list describes problems that could occur when the request is being executed, but you might also encounter other problems when the request is being made. For example, if the the request failed and the result is not available, the InvalidStateError exception is thrown.

## Notes

### Remarks

The cause of the error depends on the operation that triggered the error; use the **name** to determine the underlying problem.

### Syntax

### Standards information

-   [Indexed Database API](http://go.microsoft.com/fwlink/p/?LinkId=224519)
