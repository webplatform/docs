---
title: resolveLocalFileSystemURL
tags:
  0: API
  1: Object
  2: Methods
  4: FileSystemAPI
readiness: 'Out of Date'
standardization_status: 'W3C Working Draft'
notes:
  - 'Out of date; feature discontinued. See http://www.w3.org/TR/file-system-api/.'
summary: "Allows the user to look up the Entry for a file or directory referred to by a local URL.\n"
uri: apis/filesystem/LocalFileSystem/resolveLocalFileSystemURL

---
# resolveLocalFileSystemURL

## Summary

Allows the user to look up the Entry for a file or directory referred to by a local URL.

**Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

*Method of [apis/filesystem/LocalFileSystem](/apis/filesystem/LocalFileSystem)*

## Syntax

``` {.js}
 LocalFileSystem.resolveLocalFileSystemURL(url, successCallback, errorCallback);
```

## Parameters

### url

 Data-typeÂ
:   String

 A URL referring to a local file in a filesystem accessable via this API.

### successCallback

 Data-typeÂ
:   String

 A callback that is called to report the Entry to which the supplied URL refers.

### errorCallback

 Data-typeÂ
:   String

*(Optional)*

A callback that is called when errors happen, or when the request to obtain the Entry is denied.

## Return Value

No return value

**Needs Examples**: This section should include examples.

## Related specifications

Specification
:   Status
[W3C File API: Directories and System Specification](http://dev.w3.org/2009/dap/file-system/pub/FileSystem/)
:   W3C Working Draft

