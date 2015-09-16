---
title: 'getFile'
notes:
  - 'Out of date; feature discontinued. See http://www.w3.org/TR/file-system-api/.'
readiness: 'Out of Date'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/filesystem/DirectoryEntry
    href: /apis/filesystem/DirectoryEntry
standardization_status: 'W3C Working Draft'
summary: "Creates or looks up a file.\n"
tags:
  0: API
  1: Object
  2: Methods
  4: FileSystemAPI
uri: apis/filesystem/DirectoryEntry/getFile

---
## Summary

Creates or looks up a file.

**Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

Method of [apis/filesystem/DirectoryEntry](/apis/filesystem/DirectoryEntry)[apis/filesystem/DirectoryEntry](/apis/filesystem/DirectoryEntry)

## Syntax

``` js
 DirectoryEntry.getFile(path, options, successCallback, errorCallback);
```

## Parameters

### path

 Data-type
:   String

 Either an absolute path or a relative path from this DirectoryEntry to the file to be looked up or created. It is an error to attempt to create a file whose immediate parent does not yet exist.

### options

 Data-type
:   String

(Optional)

-   If create and exclusive are both true and the path already exists, getDirectory must fail.
-   If create is true, the path doesn't exist, and no other error occurs, getDirectory must create and return a corresponding DirectoryEntry.
-   If create is not true and the path doesn't exist, getDirectory must fail.
-   If create is not true and the path exists, but is a file, getDirectory must fail.
-   Otherwise, if no other error occurs, getDirectory must return a DirectoryEntry corresponding to path.

### successCallback

 Data-type
:   String

(Optional)

A callback that is called to return the File selected or created.

### errorCallback

 Data-type
:   String

(Optional)

A callback that is called when errors happen.

## Return Value

No return value

**Needs Examples**: This section should include examples.

## Related specifications

[W3C File API: Directories and System Specification](http://dev.w3.org/2009/dap/file-system/pub/FileSystem/)
:   W3C Working Draft
