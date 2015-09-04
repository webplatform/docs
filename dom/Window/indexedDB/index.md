---
title: indexedDB
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Provides access to the IndexedDB features supported by the browser and/or device.'
uri: dom/Window/indexedDB

---
# indexedDB

## Summary

Provides access to the IndexedDB features supported by the browser and/or device.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Window](/dom/Window)</span></span>

## Syntax

``` {.js}
var ixDBHandle = window.indexedDB;
window.indexedDB = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">IDBFactory</span></span>

A handle to the IndexedDB "factory," which allows access to IndexedDB features on the current browser/device.

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
   doIndexedDBWork();
}
```

## Notes

### Remarks

For security reasons, Internet Explorer support for the [**indexedDB**](/apis/indexeddb/IDBFactory) property is limited to webpages loaded using the "http://" or "https://" protocols.

**Note:**  In pre-release versions of Internet Explorer 10, the **indexedDB** was accessed using a vendor prefix (**msIndexedDB**). Such use is considered obsolete; applications using the vendor prefix should be updated to ensure standards-compliance and future compatibility.

## Related specifications

Specification
:   Status
[Indexed Database API](http://www.w3.org/TR/IndexedDB/)
:   Candidate Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Using indexDB](https://developer.mozilla.org/en-US/docs/Web/API/IndexedDB_API/Using_IndexedDB) Article]

Portions of this content come from the Microsoft Developer Network: [[indexDB Property](http://msdn.microsoft.com/en-us/library/ie/hh772512(v=vs.85).aspx) Article]

