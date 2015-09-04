---
title: IDBVersionChangeEvent
tags:
  0: API
  1: Objects
  3: IndexedDB
readiness: 'Ready to Use'
standardization_status: 'W3C Proposed Recommendation'
summary: 'The IDBVersionChangeEvent object represents the event object passed to the  upgradeneeded event, which fires when a database is opened using a higher version number.'
uri: apis/indexeddb/IDBVersionChangeEvent

---
# IDBVersionChangeEvent

## Summary

The IDBVersionChangeEvent object represents the event object passed to the upgradeneeded event, which fires when a database is opened using a higher version number.

## Properties

API Name
:   Summary
[newVersion](/apis/indexeddb/IDBVersionChangeEvent/newVersion)
:   Returns the new version of the database, which is the version specified by the open request.
[oldVersion](/apis/indexeddb/IDBVersionChangeEvent/oldVersion)
:   Returns the old version of the database.

## Methods

*No methods.*

## Events

*No events.*

## Examples

In this example, properties from the IDBVersionChangeEvent object passed to the [upgradeneeded](/apis/indexeddb/IDBOpenDBRequest/onUpgradeNeeded) event are used by the createDatabaseObjects function (not shown):

``` {.js}
try {
  var req = window.indexedDB.open( "MyDatabase", 1.0 );
  req.onsuccess = doDatabaseWork;
  req.onerror = handleErrorEvent;
  req.onblocked = handleBlockedEvent;
  req.onupgradeneeded = function(evt) {
    createDatabaseObjects(
       evt.target.result, evt.target.transaction,
       evt.oldVersion, evt.newVersion );
  }
} catch( ex ) {
  handleException( ex.message );
}
```

## Usage

     When you open a database, you include a version number.  If the supplied version number is greater than the version of the database on the user's device (if any), an upgradeneeded event is fired within the context of a version change transaction.  This context lets you create (or modify) object stores, indexes, ranges, and other database objects.

For more information about transaction types, see [IDBTransaction mode](/apis/indexeddb/IDBTransaction/mode).

## Notes

The [upgradeneeded](/apis/indexeddb/IDBOpenDBRequest/onUpgradeNeeded) event fires before the [success](/apis/indexeddb/IDBRequest/onsuccess) event, which can lead to issues when attempting to cache handles.

Â

## Related specifications

Specification
:   Status
[W3C IndexedDB Specification](http://www.w3.org/TR/IndexedDB/)
:   W3C Proposed Recommendation

## See also

### External resources

-   [Creating and opening IndexedDB objects](http://msdn.microsoft.com/en-us/library/jj154905.aspx)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/IndexedDB/IDBVersionChangeEvent)

Portions of this content come from the Microsoft Developer Network: [[IDBVersionChangeEvent object](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

