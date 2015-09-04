---
title: result
tags:
  0: API
  1: Object
  2: Properties
  4: IndexedDB
readiness: 'In Progress'
notes:
  - 'Needs example, spec reference, standardization status'
summary: 'Returns the result of the request. If the the request failed and the result is not available, the DOMException InvalidStateError exception is thrown.'
uri: apis/indexeddb/IDBRequest/result

---
# result

## Summary

Returns the result of the request. If the the request failed and the result is not available, the DOMException InvalidStateError exception is thrown.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/indexeddb/IDBRequest](/apis/indexeddb/IDBRequest)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = element.result;
```

**Needs Examples**: This section should include examples.

## Notes

### Remarks

The value of that **result** property depends on the original request. For example, if the original request opened a database, the value of the **result** property would be an [**IDBDatabase**](/apis/indexeddb/IDBDatabase) object.

### Syntax

### Standards information

-   [Indexed Database API](http://go.microsoft.com/fwlink/p/?LinkId=224519)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/IndexedDB/IDBRequest)

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

