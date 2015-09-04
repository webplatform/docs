---
title: newVersion
tags:
  0: API
  1: Object
  2: Properties
  4: IndexedDB
readiness: 'In Progress'
notes:
  - 'Needs example, spec reference, standardization status'
summary: 'Returns the new version of the database, which is the version specified by the open request.'
uri: apis/indexeddb/IDBVersionChangeEvent/newVersion
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - apis/indexedDB/IDBVersionChangeEvent

---
# newVersion

## Summary

Returns the new version of the database, which is the version specified by the open request.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/indexeddb/IDBVersionChangeEvent](/apis/indexeddb/IDBVersionChangeEvent)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = element.newVersion;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">unsigned long</span></span>

A number corresponding to the value specified in the [IDBFactory.open](/apis/indexeddb/IDBFactory/open) request.

**Needs Examples**: This section should include examples.

## See also

### Related pages (MSDN)

-   `IDBVersionChangeEvent`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/IndexedDB/IDBVersionChangeEvent)

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

