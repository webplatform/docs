---
title: indexedDB
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Using indexDB](https://developer.mozilla.org/en-US/docs/Web/API/IndexedDB_API/Using_IndexedDB) Article]'
  - 'Microsoft Developer Network: [[indexDB Property](http://msdn.microsoft.com/en-us/library/ie/hh772512(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Window
    href: /dom/Window
  return:
    predicate: 'Returns an object of type '
    value: IDBFactory
    href: /dom/Window
standardization_status: 'W3C Candidate Recommendation'
summary: 'Provides access to the IndexedDB features supported by the browser and/or device.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Window/indexedDB

---
## <span>Summary</span>

Provides access to the IndexedDB features supported by the browser and/or device.

Property of [dom/Window](/dom/Window)[dom/Window](/dom/Window)

## <span>Syntax</span>

``` js
var ixDBHandle = window.indexedDB;
window.indexedDB = value;
```

## <span>Return Value</span>

Returns an object of type IDBFactoryIDBFactory

A handle to the IndexedDB "factory," which allows access to IndexedDB features on the current browser/device.

## <span>Examples</span>

The following example uses feature detection to determine whether IndexedDB is supported by the current browser/device.

``` js
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

## <span>Notes</span>

### <span>Remarks</span>

For security reasons, Internet Explorer support for the [**indexedDB**](/apis/indexeddb/IDBFactory) property is limited to webpages loaded using the "http://" or "https://" protocols.

**Note:**  In pre-release versions of Internet Explorer 10, the **indexedDB** was accessed using a vendor prefix (**msIndexedDB**). Such use is considered obsolete; applications using the vendor prefix should be updated to ensure standards-compliance and future compatibility.

## <span>Related specifications</span>

[Indexed Database API](http://www.w3.org/TR/IndexedDB/)
:   Candidate Recommendation
