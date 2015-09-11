---
title: getParent
notes:
  - 'Out of date; feature discontinued. See http://www.w3.org/TR/file-system-api/.'
readiness: 'Out of Date'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/filesystem/EntrySync
    href: /apis/filesystem/EntrySync
  return_type:
    predicate: 'Returns an object of type  '
    value: ''
    href: /apis/filesystem/EntrySync
standardization_status: 'W3C Working Draft'
summary: "Look up the parent DirectoryEntrySync containing this EntrySync. If this EntrySync is the root of its filesystem, its parent is itself.\n"
tags:
  0: API
  1: Object
  2: Methods
  4: FileSystemAPI
uri: apis/filesystem/EntrySync/getParent

---
## <span>Summary</span>

Look up the parent DirectoryEntrySync containing this EntrySync. If this EntrySync is the root of its filesystem, its parent is itself.

**Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

Method of [apis/filesystem/EntrySync](/apis/filesystem/EntrySync)[apis/filesystem/EntrySync](/apis/filesystem/EntrySync)

## <span>Syntax</span>

``` js
var  = EntrySync.getParent();
```

## <span>Return Value</span>

Returns an object of type<span></span>

DirectoryEntrySync

**Needs Examples**: This section should include examples.

## <span>Related specifications</span>

[W3C File API: Directories and System Specification](http://dev.w3.org/2009/dap/file-system/pub/FileSystem/)
:   W3C Working Draft
