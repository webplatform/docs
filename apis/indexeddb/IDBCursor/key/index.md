---
title: key
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs example, spec reference, standardization status'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/indexeddb/IDBCursor
    href: /apis/indexeddb/IDBCursor
  return:
    predicate: 'Returns an object of type '
    value: any
    href: /apis/indexeddb/IDBCursor
standardization_status: 'W3C Working Draft'
summary: 'The key value for the record currently displayed by the cursor.'
tags:
  0: API
  1: Object
  2: Properties
  4: IndexedDB
uri: apis/indexeddb/IDBCursor/key

---
## <span>Summary</span>

The key value for the record currently displayed by the cursor.

Property of [apis/indexeddb/IDBCursor](/apis/indexeddb/IDBCursor)[apis/indexeddb/IDBCursor](/apis/indexeddb/IDBCursor)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = cursor.key;
```

## <span>Return Value</span>

Returns an object of type anyany

The value depends on the source of the value. For more info, see the following Notes section.

**Needs Examples**: This section should include examples.

## <span>Notes</span>

### <span>Remarks</span>

The value of the **key** property depends on the **source** of the **cursor**.

If the cursor is opened using an index, the return value represents the value of the attribute associated with the index. If the cursor is opened using an obejct store, the return value represents the record's primary key. If the cursor record is iterating to a new record or is outside the range of the cursor, the return value is "undefined".

### <span>Syntax</span>

### <span>Standards information</span>

-   [Indexed Database API](http://go.microsoft.com/fwlink/p/?LinkId=224519)
