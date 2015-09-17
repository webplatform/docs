---
title: 'createWriter'
notes:
  - 'Out of date; feature discontinued. See http://www.w3.org/TR/file-system-api/.'
readiness: 'Out of Date'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/filesystem/FileEntry
    href: /apis/filesystem/FileEntry
standardization_status: 'W3C Working Draft'
summary: "Creates a new FileWriter associated with the file that this FileEntry represents.\n"
tags:
  - API_Object_Methods
  - API
  - FileSystemAPI
  - Needs_Examples
uri: apis/filesystem/FileEntry/createWriter

---
## Summary

Creates a new FileWriter associated with the file that this FileEntry represents.

**Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

Method of [apis/filesystem/FileEntry](/apis/filesystem/FileEntry)[apis/filesystem/FileEntry](/apis/filesystem/FileEntry)

## Syntax

``` js
 FileEntry.createWriter(successCallback, errorCallback);
```

## Parameters

### successCallback

 Data-type
:   String

 A callback that is called with the new FileWriter.

### errorCallback

 Data-type
:   String

(Optional)

A callback that is called when errors happen.

## Return Value

No return value

## Related specifications

[W3C Web Audio API](http://dev.w3.org/2009/dap/file-system/pub/FileSystem/)
:   W3C Working Draft
