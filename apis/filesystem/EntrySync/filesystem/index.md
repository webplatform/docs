---
title: 'filesystem'
notes:
  - 'Out of date; feature discontinued. See http://www.w3.org/TR/file-system-api/.'
readiness: 'Out of Date'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/filesystem/EntrySync
    href: /apis/filesystem/EntrySync
  return:
    predicate: 'Returns an object of type '
    value: ''
    href: /apis/filesystem/EntrySync
standardization_status: 'W3C Working Draft'
summary: "The file system on which the EntrySync resides.\n"
tags:
  0: API
  1: Object
  2: Properties
  4: FileSystemAPI
uri: apis/filesystem/EntrySync/filesystem

---
## Summary

The file system on which the EntrySync resides.

**Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

Property of [apis/filesystem/EntrySync](/apis/filesystem/EntrySync)[apis/filesystem/EntrySync](/apis/filesystem/EntrySync)

## Syntax

**Note**: This property is read-only.

``` js
var result = EntrySync.filesystem;
```

## Return Value

Returns an object of type

Filesystem

**Needs Examples**: This section should include examples.

## Related specifications

[W3C File API: Directories and System Specification](http://dev.w3.org/2009/dap/file-system/pub/FileSystem/)
:   W3C Working Draft
