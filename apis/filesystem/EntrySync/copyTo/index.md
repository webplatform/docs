---
title: 'copyTo'
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
summary: "Copy an EntrySync to a different location on the file system.\n"
tags:
  0: API
  1: Object
  2: Methods
  4: FileSystemAPI
uri: apis/filesystem/EntrySync/copyTo

---
## Summary

Copy an EntrySync to a different location on the file system.

**Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

Method of [apis/filesystem/EntrySync](/apis/filesystem/EntrySync)[apis/filesystem/EntrySync](/apis/filesystem/EntrySync)

## Syntax

``` js
var  = EntrySync.copyTo(parent, newName);
```

## Parameters

### parent

 Data-type
:   String

 The directory to which to move the EntrySync.

### newName

 Data-type
:   String

(Optional)

The new name of the EntrySync. Defaults to the EntrySync's current name if unspecified.

## Return Value

Returns an object of type

EntrySync

**Needs Examples**: This section should include examples.

## Notes

It is an error to try to:

-   copy a directory inside itself or to any child at any depth;
-   copy an EntrySync into its parent if a name different from its current one isn't provided;
-   copy a file to a path occupied by a directory;
-   copy a directory to a path occupied by a file;
-   copy any element to a path occupied by a directory which is not empty.

A copy of a file on top of an existing file must attempt to delete and replace that file.

A copy of a directory on top of an existing empty directory must attempt to delete and replace that directory.

Directory copies are always recursive--that is, they copy all contents of the directory.

## Related specifications

[W3C File API: Directories and System Specification](http://dev.w3.org/2009/dap/file-system/pub/FileSystem/)
:   W3C Working Draft
