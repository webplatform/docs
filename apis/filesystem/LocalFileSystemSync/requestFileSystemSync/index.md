---
title: requestFileSystemSync
notes:
  - 'Out of date; feature discontinued. See http://www.w3.org/TR/file-system-api/.'
readiness: 'Out of Date'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/filesystem/LocalFileSystemSync
    href: /apis/filesystem/LocalFileSystemSync
  return_type:
    predicate: 'Returns an object of type  '
    value: ''
    href: /apis/filesystem/LocalFileSystemSync
standardization_status: 'W3C Working Draft'
summary: "Requests a file system where data should be stored. You access a sandboxed file system by requesting a LocalFileSystemSync object from within a web worker using this global method, window.requestFileSystemSync().\n"
tags:
  0: API
  1: Object
  2: Methods
  4: FileSystemAPI
uri: apis/filesystem/LocalFileSystemSync/requestFileSystemSync

---
## Summary

Requests a file system where data should be stored. You access a sandboxed file system by requesting a LocalFileSystemSync object from within a web worker using this global method, window.requestFileSystemSync().

**Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

Method of [apis/filesystem/LocalFileSystemSync](/apis/filesystem/LocalFileSystemSync)[apis/filesystem/LocalFileSystemSync](/apis/filesystem/LocalFileSystemSync)

## Syntax

``` js
var  = LocalFileSystemSync.requestFileSystemSync(type, size);
```

## Parameters

### type

 Data-type
:   unsigned short

 Whether the filesystem requested should be persistent. Use one of TEMPORARY (0) or PERSISTENT (1).

### size

 Data-type
:   unsigned long

 How much storage space, in bytes, the application expects to need.

## Return Value

Returns an object of type

FileSystemSync

**Needs Examples**: This section should include examples.

## Related specifications

[W3C File API: Directories and System Specification](http://dev.w3.org/2009/dap/file-system/pub/FileSystem/)
:   W3C Working Draft
