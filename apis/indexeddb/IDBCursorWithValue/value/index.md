---
title: value
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary, example, spec reference, standardization status'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/indexeddb/IDBCursorWithValue
    href: /apis/indexeddb/IDBCursorWithValue
tags:
  0: API
  1: Object
  2: Properties
  4: IndexedDB
uri: apis/indexeddb/IDBCursorWithValue/value

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Property of [apis/indexeddb/IDBCursorWithValue](/apis/indexeddb/IDBCursorWithValue)[apis/indexeddb/IDBCursorWithValue](/apis/indexeddb/IDBCursorWithValue)

## Syntax

**Note**: This property is read-only.

``` js
var result = element.value;
```

**Needs Examples**: This section should include examples.

## Notes

### Remarks

If the result is an object, the object remains the same until the cursor iterates to a new record. Changes to the results of the **value** property are visible to the object variable, but are not saved in the underlying object store.

### Syntax

### Standards information

-   [Indexed Database API](http://go.microsoft.com/fwlink/p/?LinkId=224519)
