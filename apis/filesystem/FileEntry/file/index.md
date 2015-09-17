---
title: 'file'
notes:
  - 'Out of date; feature discontinued. See http://www.w3.org/TR/file-system-api/.'
readiness: 'Out of Date'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/filesystem/FileEntry
    href: /apis/filesystem/FileEntry
standardization_status: 'W3C Working Draft'
summary: "Returns a File that represents the current state of the file that this FileEntry represents.\n"
tags:
  - API_Object_Methods
  - API
  - FileSystemAPI
  - Needs_Examples
uri: apis/filesystem/FileEntry/file

---
## Summary

Returns a File that represents the current state of the file that this FileEntry represents.

**Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

Method of [apis/filesystem/FileEntry](/apis/filesystem/FileEntry)[apis/filesystem/FileEntry](/apis/filesystem/FileEntry)

## Syntax

``` js
 FileEntry.file(successCallback, errorCallback);
```

## Parameters

### successCallback

 Data-type
:   String

 A callback that is called with the File.

### errorCallback

 Data-type
:   String

(Optional)

A callback that is called when errors happen.

## Return Value

No return value

## Related specifications

[W3C File API: Directories and System Specification](http://dev.w3.org/2009/dap/file-system/pub/FileSystem/)
:   W3C Working Draft
