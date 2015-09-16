---
title: resolveLocalFileSystemSyncURL
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
summary: "Allows the user to look up the Entry for a file or directory referred to by a local URL.\n"
tags:
  0: API
  1: Object
  2: Methods
  4: FileSystemAPI
uri: apis/filesystem/LocalFileSystemSync/resolveLocalFileSystemSyncURL

---
## Summary

Allows the user to look up the Entry for a file or directory referred to by a local URL.

**Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

Method of [apis/filesystem/LocalFileSystemSync](/apis/filesystem/LocalFileSystemSync)[apis/filesystem/LocalFileSystemSync](/apis/filesystem/LocalFileSystemSync)

## Syntax

``` js
var  = LocalFileSystemSync.resolveLocalFileSystemSyncURL(url);
```

## Parameters

### url

 Data-type
:   String

 A URL referring to a local file in a filesystem accessable via this API.

## Return Value

Returns an object of type

EntrySync

**Needs Examples**: This section should include examples.

## Related specifications

[W3C File API: Directories and System Specification](http://dev.w3.org/2009/dap/file-system/pub/FileSystem/)
:   W3C Working Draft
