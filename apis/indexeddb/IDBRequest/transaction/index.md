---
title: transaction
tags:
  0: API
  1: Object
  2: Properties
  4: IndexedDB
readiness: 'In Progress'
standardization_status: 'W3C Proposed Recommendation'
notes:
  - 'Needs example, spec reference'
summary: 'The transaction for the request. This property can be null for certain requests, such as for request returned from IDBFactory.open (You''re just connecting to a database, so there is no transaction to return).'
uri: apis/indexeddb/IDBRequest/transaction

---
# transaction

## Summary

The transaction for the request. This property can be null for certain requests, such as for request returned from IDBFactory.open (You're just connecting to a database, so there is no transaction to return).

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/indexeddb/IDBRequest](/apis/indexeddb/IDBRequest)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = element.transaction;
```

**Needs Examples**: This section should include examples.

### Syntax

### Standards information

-   [Indexed Database API](http://go.microsoft.com/fwlink/p/?LinkId=224519)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/IndexedDB/IDBRequest)

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

