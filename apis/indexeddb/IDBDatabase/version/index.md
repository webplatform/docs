---
title: version
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs example, spec reference, standardization status'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/indexeddb/IDBDatabase
    href: /apis/indexeddb/IDBDatabase
summary: 'Returns the version of the database when this IDBDatabaseSync instance was created.'
tags:
  0: API
  1: Object
  2: Properties
  4: IndexedDB
uri: apis/indexeddb/IDBDatabase/version

---
## <span>Summary</span>

Returns the version of the database when this IDBDatabaseSync instance was created.

Property of [apis/indexeddb/IDBDatabase](/apis/indexeddb/IDBDatabase)[apis/indexeddb/IDBDatabase](/apis/indexeddb/IDBDatabase)

## <span>Syntax</span>

``` js
var result = element.version;
element.version = value;
```

**Needs Examples**: This section should include examples.

## <span>Notes</span>

### <span>Remarks</span>

In pre-release versions of Internet Explorer 10, this property initially returned a **DOMString** value. Based on changes to the underlying specification, the **version** property now returns a **unsigned long long** value. Applications that rely on the original implementation must be updated accordingly.

### <span>Syntax</span>

### <span>Standards information</span>

-   [Indexed Database API](http://go.microsoft.com/fwlink/p/?LinkId=224519)
