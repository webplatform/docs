---
title: onblocked
tags:
  0: API
  1: Object
  2: Properties
  4: IndexedDB
readiness: 'In Progress'
notes:
  - 'Needs example, spec reference, standardization status'
summary: 'The event handler for the blocked event. This event is triggered when the upgradeneeded should be triggered because of a version change but the database is still in use (ie not closed) somewhere, even after the versionchange event was sent.'
uri: apis/indexeddb/IDBOpenDBRequest/onblocked

---
# onblocked

## Summary

The event handler for the blocked event. This event is triggered when the upgradeneeded should be triggered because of a version change but the database is still in use (ie not closed) somewhere, even after the versionchange event was sent.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/indexeddb/IDBOpenDBRequest](/apis/indexeddb/IDBOpenDBRequest)</span></span>

## Syntax

``` {.js}
var result = element.onblocked;
element.onblocked = value;
```

**Needs Examples**: This section should include examples.

