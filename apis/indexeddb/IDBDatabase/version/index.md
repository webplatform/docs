---
title: version
tags:
  0: API
  1: Object
  2: Properties
  4: IndexedDB
readiness: 'In Progress'
notes:
  - 'Needs example, spec reference, standardization status'
summary: 'Returns the version of the database when this IDBDatabaseSync instance was created.'
uri: apis/indexeddb/IDBDatabase/version

---
# version

## Summary

Returns the version of the database when this IDBDatabaseSync instance was created.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/indexeddb/IDBDatabase](/apis/indexeddb/IDBDatabase)</span></span>

## Syntax

``` {.js}
var result = element.version;
element.version = value;
```

**Needs Examples**: This section should include examples.

## Notes

### Remarks

In pre-release versions of Internet Explorer 10, this property initially returned a **DOMString** value. Based on changes to the underlying specification, the **version** property now returns a **unsigned long long** value. Applications that rely on the original implementation must be updated accordingly.

### Syntax

### Standards information

-   [Indexed Database API](http://go.microsoft.com/fwlink/p/?LinkId=224519)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

