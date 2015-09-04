---
title: DirectoryReader
tags:
  0: API
  1: Objects
  3: FileSystemAPI
readiness: 'Out of Date'
standardization_status: 'W3C Working Draft'
notes:
  - 'Out of date; feature discontinued. See http://www.w3.org/TR/file-system-api/.'
summary: "This interface lets a user list files and directories in a directory.\n"
uri: apis/filesystem/DirectoryReader

---
# DirectoryReader

## Summary

This interface lets a user list files and directories in a directory.

**Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

## Properties

*No properties.*

## Methods

API Name
:   Summary
[readEntries](/apis/filesystem/DirectoryReader/readEntries)
:   Read the next block of entries from this directory.

    **Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

## Events

*No events.*

## Notes

If there are no additions to or deletions from a directory between the first and last call to readEntries, and no errors occur, then:

-   A series of calls to readEntries must return each entry in the directory exactly once.
-   Once all entries have been returned, the next call to readEntries must produce an empty array.
-   If not all entries have been returned, the array produced by readEntries must not be empty.
-   The entries produced by readEntries must not include the directory itself ["."] or its parent [".."].

## Related specifications

Specification
:   Status
[W3C File API: Directories and System Specification](http://dev.w3.org/2009/dap/file-system/pub/FileSystem/)
:   W3C Working Draft

