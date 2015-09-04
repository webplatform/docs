---
title: IDBKeyRange
tags:
  0: API
  1: Objects
  3: IndexedDB
readiness: 'Ready to Use'
standardization_status: 'W3C Proposed Recommendation'
summary: 'A range of keys defined for an object store or index.'
uri: apis/indexeddb/IDBKeyRange

---
# IDBKeyRange

## Summary

A range of keys defined for an object store or index.

## Properties

API Name
:   Summary
[lower](/apis/indexeddb/IDBKeyRange/lower)
:   This value is the lower-bound of the key range.
[lowerOpen](/apis/indexeddb/IDBKeyRange/lowerOpen)
:   Returns false if the lower-bound value is included in the key range. Returns true if the lower-bound value is excluded from the key range.
[upperOpen](/apis/indexeddb/IDBKeyRange/upperOpen)
:   Returns false if the upper-bound value is included in the key range. Returns true if the upper-bound value is excluded from the key range.

## Methods

API Name
:   Summary
[bound](/apis/indexeddb/IDBKeyRange/bound)
:   Creates and returns a new key range with lower set to *lower*, lowerOpen set to *lowerOpen*, upper set to *upper* and upperOpen set to *upperOpen*.
[lowerBound](/apis/indexeddb/IDBKeyRange/lowerBound)
:   Creates and returns a new key range with lower set to lower, lowerOpen set to open, upper set to undefined and and upperOpen set to true.
[only](/apis/indexeddb/IDBKeyRange/only)
:   Creates and returns a new key range with both lower and upper set to value and both lowerOpen and upperOpen set to false.
[upperBound](/apis/indexeddb/IDBKeyRange/upperBound)
:   Creates and returns a new key range with lower set to undefined, lowerOpen set to true, upper set to upper and and upperOpen set to open.

## Events

*No events.*

## Related specifications

Specification
:   Status
[W3C IndexedDB Specification](http://www.w3.org/TR/IndexedDB/)
:   W3C Proposed Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

