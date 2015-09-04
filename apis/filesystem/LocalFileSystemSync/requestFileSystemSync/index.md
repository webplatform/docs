---
title: requestFileSystemSync
tags:
  0: API
  1: Object
  2: Methods
  4: FileSystemAPI
readiness: 'Out of Date'
standardization_status: 'W3C Working Draft'
notes:
  - 'Out of date; feature discontinued. See http://www.w3.org/TR/file-system-api/.'
summary: "Requests a file system where data should be stored. You access a sandboxed file system by requesting a LocalFileSystemSync object from within a web worker using this global method, window.requestFileSystemSync().\n"
uri: apis/filesystem/LocalFileSystemSync/requestFileSystemSync

---
# requestFileSystemSync

## Summary

Requests a file system where data should be stored. You access a sandboxed file system by requesting a LocalFileSystemSync object from within a web worker using this global method, window.requestFileSystemSync().

**Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

*Method of [apis/filesystem/LocalFileSystemSync](/apis/filesystem/LocalFileSystemSync)*

## Syntax

``` {.js}
var  = LocalFileSystemSync.requestFileSystemSync(type, size);
```

## Parameters

### type

 Data-typeÂ
:   unsigned short

 Whether the filesystem requested should be persistent. Use one of TEMPORARY (0) or PERSISTENT (1).

### size

 Data-typeÂ
:   unsigned long

 How much storage space, in bytes, the application expects to need.

## Return Value

Returns an object of type .

FileSystemSync

**Needs Examples**: This section should include examples.

## Related specifications

Specification
:   Status
[W3C File API: Directories and System Specification](http://dev.w3.org/2009/dap/file-system/pub/FileSystem/)
:   W3C Working Draft

