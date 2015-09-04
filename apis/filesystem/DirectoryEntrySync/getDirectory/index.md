---
title: getDirectory
tags:
  0: API
  1: Object
  2: Methods
  4: FileSystemAPI
readiness: 'Out of Date'
standardization_status: 'W3C Working Draft'
notes:
  - 'Out of date; feature discontinued. See http://www.w3.org/TR/file-system-api/.'
summary: "Creates or looks up a directory.\n"
uri: apis/filesystem/DirectoryEntrySync/getDirectory

---
# getDirectory

## Summary

Creates or looks up a directory.

**Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

*Method of [apis/filesystem/DirectoryEntrySync](/apis/filesystem/DirectoryEntrySync)*

## Syntax

``` {.js}
var  = DirectoryEntrySync.getDirectory(path, options);
```

## Parameters

### path

 Data-typeÂ
:   String

 Either an absolute path or a relative path from this DirectoryEntrySync to the directory to be looked up or created. It is an error to attempt to create a directory whose immediate parent does not yet exist.

### options

 Data-typeÂ
:   String

*(Optional)*

-   If create and exclusive are both true and the path already exists, getDirectory must fail.
-   If create is true, the path doesn't exist, and no other error occurs, getDirectory must create and return a corresponding DirectoryEntry.
-   If create is not true and the path doesn't exist, getDirectory must fail.
-   If create is not true and the path exists, but is a file, getDirectory must fail.
-   Otherwise, if no other error occurs, getDirectory must return a DirectoryEntrySync corresponding to path.

## Return Value

Returns an object of type .

DirectoryEntrySync

**Needs Examples**: This section should include examples.

## Related specifications

Specification
:   Status
[W3C File API: Directories and System Specification](http://dev.w3.org/2009/dap/file-system/pub/FileSystem/)
:   W3C Working Draft

