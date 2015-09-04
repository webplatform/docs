---
title: removeRecursively
tags:
  0: API
  1: Object
  2: Methods
  4: FileSystemAPI
readiness: 'Out of Date'
standardization_status: 'W3C Working Draft'
notes:
  - 'Out of date; feature discontinued. See http://www.w3.org/TR/file-system-api/.'
summary: "Deletes a directory and all of its contents, if any. In the event of an error [e.g. trying to delete a directory that contains a file that cannot be removed], some of the contents of the directory may be deleted. It is an error to attempt to delete the root directory of a filesystem.\n"
uri: apis/filesystem/DirectoryEntrySync/removeRecursively

---
# removeRecursively

## Summary

Deletes a directory and all of its contents, if any. In the event of an error [e.g. trying to delete a directory that contains a file that cannot be removed], some of the contents of the directory may be deleted. It is an error to attempt to delete the root directory of a filesystem.

**Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

*Method of [apis/filesystem/DirectoryEntrySync](/apis/filesystem/DirectoryEntrySync)*

## Syntax

``` {.js}
 DirectoryEntrySync.removeRecursively();
```

## Return Value

No return value

**Needs Examples**: This section should include examples.

## Related specifications

Specification
:   Status
[W3C File API: Directories and System Specification](http://dev.w3.org/2009/dap/file-system/pub/FileSystem/)
:   W3C Working Draft

