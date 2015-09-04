---
title: mode
tags:
  0: API
  1: Object
  2: Properties
  4: IndexedDB
readiness: 'In Progress'
notes:
  - 'Needs example, spec reference, standardization status'
summary: 'The mode for isolating access to data in the object stores that are in the scope of the transaction. For possible values, see Return Value, below. The default value is readonly.'
uri: apis/indexeddb/IDBTransaction/mode

---
# mode

## Summary

The mode for isolating access to data in the object stores that are in the scope of the transaction. For possible values, see Return Value, below. The default value is readonly.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/indexeddb/IDBTransaction](/apis/indexeddb/IDBTransaction)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = element.mode;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

-   readonly (0) - Allows data to be read but not changed.
-   readwrite (1) - Allows reading and writing of data in existing data stores to be changed.
-   versionchange (2) - Allows any operation to be performed, including ones that delete and create object stores and indexes. This mode is for updating the version number of transactions that were started using the setVersion() method of IDBDatabase objects. Transactions of this mode cannot run concurrently with other transactions.

**Needs Examples**: This section should include examples.

### Syntax

### Standards information

-   [Indexed Database API](http://go.microsoft.com/fwlink/p/?LinkId=224519)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/IndexedDB/IDBTransaction)

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

