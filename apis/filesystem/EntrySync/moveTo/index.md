---
title: moveTo
tags:
  0: API
  1: Object
  2: Methods
  4: FileSystemAPI
readiness: 'Out of Date'
standardization_status: 'W3C Working Draft'
notes:
  - 'Out of date; feature discontinued. See http://www.w3.org/TR/file-system-api/.'
summary: "Move an EntrySync to a different location on the file system.\n"
uri: apis/filesystem/EntrySync/moveTo

---
# moveTo

## Summary

Move an EntrySync to a different location on the file system.

**Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

*Method of [apis/filesystem/EntrySync](/apis/filesystem/EntrySync)*

## Syntax

``` {.js}
var  = EntrySync.moveTo(parent, newName);
```

## Parameters

### parent

 Data-typeÂ
:   String

 The directory to which to move the EntrySync.

### newName

 Data-typeÂ
:   String

*(Optional)*

The new name of the EntrySync. Defaults to the EntrySync's current name if unspecified.

## Return Value

Returns an object of type .

EntrySync

**Needs Examples**: This section should include examples.

## Notes

It is an error to try to:

-   move a directory inside itself or to any child at any depth;
-   move an entry into its parent if a name different from its current one isn't provided;
-   move a file to a path occupied by a directory;
-   move a directory to a path occupied by a file;
-   move any element to a path occupied by a directory which is not empty.

A move of a file on top of an existing file must attempt to delete and replace that file.

A move of a directory on top of an existing empty directory must attempt to delete and replace that directory.

## Related specifications

Specification
:   Status
[W3C File API: Directories and System Specification](http://dev.w3.org/2009/dap/file-system/pub/FileSystem/)
:   W3C Working Draft

