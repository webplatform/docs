---
title: remove
tags:
  0: API
  1: Object
  2: Methods
  4: FileSystemAPI
readiness: 'Out of Date'
standardization_status: 'W3C Working Draft'
notes:
  - 'Out of date; feature discontinued. See http://www.w3.org/TR/file-system-api/.'
summary: "Deletes a file or directory.\n"
uri: apis/filesystem/EntrySync/remove

---
# remove

## Summary

Deletes a file or directory.

**Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

*Method of [apis/filesystem/EntrySync](/apis/filesystem/EntrySync)*

## Syntax

``` {.js}
 EntrySync.remove();
```

## Return Value

No return value

**Needs Examples**: This section should include examples.

## Notes

It is an error to attempt to delete a directory that is not empty.

It is an error to attempt to delete the root directory of a filesystem.

## Related specifications

Specification
:   Status
[W3C File API: Directories and System Specification](http://dev.w3.org/2009/dap/file-system/pub/FileSystem/)
:   W3C Working Draft

