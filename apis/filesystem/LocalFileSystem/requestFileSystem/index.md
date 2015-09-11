---
title: requestFileSystem
notes:
  - 'Out of date; feature discontinued. See http://www.w3.org/TR/file-system-api/.'
readiness: 'Out of Date'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/filesystem/LocalFileSystem
    href: /apis/filesystem/LocalFileSystem
standardization_status: 'W3C Working Draft'
summary: "Requests a file system where data should be stored. You access a sandboxed file system by requesting a LocalFileSystem object using this global method, window.requestFileSystem().\n"
tags:
  0: API
  1: Object
  2: Methods
  4: FileSystemAPI
uri: apis/filesystem/LocalFileSystem/requestFileSystem

---
## <span>Summary</span>

Requests a file system where data should be stored. You access a sandboxed file system by requesting a LocalFileSystem object using this global method, window.requestFileSystem().

**Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

Method of [apis/filesystem/LocalFileSystem](/apis/filesystem/LocalFileSystem)[apis/filesystem/LocalFileSystem](/apis/filesystem/LocalFileSystem)

## <span>Syntax</span>

``` js
 LocalFileSystem.requestFileSystem(type, size, successCallback, errorCallback);
```

## <span>Parameters</span>

### <span>type</span>

 Data-type
:   unsigned short

 Whether the filesystem requested should be persistent. Use one of TEMPORARY (0) or PERSISTENT (1).

### <span>size</span>

 Data-type
:   unsigned long

 How much storage space, in bytes, the application expects to need.

### <span>successCallback</span>

 Data-type
:   String

 The callback that is called when the user agent provides a filesystem.

### <span>errorCallback</span>

 Data-type
:   String

(Optional)

The callback that is called when errors happen, or when the request to obtain the filesystem is denied.

## <span>Return Value</span>

No return value

**Needs Examples**: This section should include examples.

## <span>Related specifications</span>

[W3C File API: Directories and System Specification](http://dev.w3.org/2009/dap/file-system/pub/FileSystem/)
:   W3C Working Draft
