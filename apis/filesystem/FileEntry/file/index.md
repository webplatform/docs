---
title: file
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
  0: API
  1: Object
  2: Methods
  4: FileSystemAPI
uri: apis/filesystem/FileEntry/file

---
## <span>Summary</span>

Returns a File that represents the current state of the file that this FileEntry represents.

**Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

Method of [apis/filesystem/FileEntry](/apis/filesystem/FileEntry)[apis/filesystem/FileEntry](/apis/filesystem/FileEntry)

## <span>Syntax</span>

``` js
 FileEntry.file(successCallback, errorCallback);
```

## <span>Parameters</span>

### <span>successCallback</span>

 Data-type
:   String

 A callback that is called with the File.

### <span>errorCallback</span>

 Data-type
:   String

(Optional)

A callback that is called when errors happen.

## <span>Return Value</span>

No return value

**Needs Examples**: This section should include examples.

## <span>Related specifications</span>

[W3C File API: Directories and System Specification](http://dev.w3.org/2009/dap/file-system/pub/FileSystem/)
:   W3C Working Draft
