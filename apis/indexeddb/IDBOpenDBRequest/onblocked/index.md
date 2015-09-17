---
title: 'onblocked'
notes:
  - 'Needs example, spec reference, standardization status'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/indexeddb/IDBOpenDBRequest
    href: /apis/indexeddb/IDBOpenDBRequest
summary: 'The event handler for the blocked event. This event is triggered when the upgradeneeded should be triggered because of a version change but the database is still in use (ie not closed) somewhere, even after the versionchange event was sent.'
tags:
  - API_Object_Properties
  - API
  - IndexedDB
  - Needs_Examples
uri: apis/indexeddb/IDBOpenDBRequest/onblocked

---
## Summary

The event handler for the blocked event. This event is triggered when the upgradeneeded should be triggered because of a version change but the database is still in use (ie not closed) somewhere, even after the versionchange event was sent.

Property of [apis/indexeddb/IDBOpenDBRequest](/apis/indexeddb/IDBOpenDBRequest)[apis/indexeddb/IDBOpenDBRequest](/apis/indexeddb/IDBOpenDBRequest)

## Syntax

``` js
var result = element.onblocked;
element.onblocked = value;
```

