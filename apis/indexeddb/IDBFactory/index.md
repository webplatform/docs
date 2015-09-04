---
title: IDBFactory
tags:
  0: API
  1: Objects
  3: IndexedDB
readiness: 'Ready to Use'
standardization_status: 'W3C Proposed Recommendation'
summary: 'The object type for the indexedDB property, which provides access to the IndexedDB features supported by the browser and/or device.'
uri: apis/indexeddb/IDBFactory

---
# IDBFactory

## Summary

The object type for the indexedDB property, which provides access to the IndexedDB features supported by the browser and/or device.

## Properties

*No properties.*

## Methods

API Name
:   Summary
[cmp](/apis/indexeddb/IDBFactory/cmp)
:   This method compares two specified keys. Returns 1 if the first key is greater than the second, -1 if the first is less than the second, and 0 if the first is equal to the second.
[deleteDatabase](/apis/indexeddb/IDBFactory/deleteDatabase)
:   Deletes a database with the specified name.
[open](/apis/indexeddb/IDBFactory/open)
:   The open method is used to open an IndexedDB database.

## Events

*No events.*

## Examples

The following example uses feature detection to determine whether IndexedDB is supported by the current browser/device.

``` {.js}
function getIndexedDBHandle() {
   var oResult = null;
   if ( window.indexedDB ) {
      oResult = window.indexedDB;
   } else if ( window.mozIndexedDB ) {
      oResult = window.mozIndexedDB;
   } else if ( window.webkitIndexedDB ) {
      oResult = window.webkitIndexedDB;
   }
   return oResult;
}

var ixHandle = getIndexedDBHandle();
if ( getIndexHandle == null ) {
   doFallback();
} else {
   doIndexedDBWork(};
}
```

## Notes

### Remarks

Use the [**indexedDB**](/apis/indexeddb/indexedDB) property to access IndexedDB databases.

**Important**  For security reasons, Internet Explorer support for the **indexedDB** property is limited to webpages loaded using the "http://" or "https://" protocols.

## Related specifications

Specification
:   Status
[W3C IndexedDB Specification](http://www.w3.org/TR/IndexedDB/)
:   W3C Proposed Recommendation

## See also

### External resources

-   [How to create a tag cloud using IndexedDB](http://msdn.microsoft.com/en-us/library/jj154908.aspx)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

}

 }