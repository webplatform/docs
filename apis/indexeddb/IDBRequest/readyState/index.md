---
title: readyState
tags:
  0: API
  1: Object
  2: Properties
  4: IndexedDB
readiness: 'In Progress'
notes:
  - 'Needs example, spec reference, standardization status'
summary: 'The state of the request. Every request starts in the pending state. The state changes to done when the request completes successfully or when an error occurs.'
uri: apis/indexeddb/IDBRequest/readyState

---
# readyState

## Summary

The state of the request. Every request starts in the pending state. The state changes to done when the request completes successfully or when an error occurs.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/indexeddb/IDBRequest](/apis/indexeddb/IDBRequest)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = element.readyState;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">enum</span></span>

-   pending (1) - The request has been started, but its result is not yet available.
-   done (2) - The request has completed or an error has occurred. Initially false.

**Needs Examples**: This section should include examples.

### Syntax

### Standards information

-   [Indexed Database API](http://go.microsoft.com/fwlink/p/?LinkId=224519)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/IndexedDB/IDBRequest)

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

