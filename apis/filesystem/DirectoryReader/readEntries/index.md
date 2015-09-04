---
title: readEntries
tags:
  0: API
  1: Object
  2: Methods
  4: FileSystemAPI
readiness: 'Out of Date'
standardization_status: 'W3C Working Draft'
notes:
  - 'Out of date; feature discontinued. See http://www.w3.org/TR/file-system-api/.'
summary: "Read the next block of entries from this directory.\n"
uri: apis/filesystem/DirectoryReader/readEntries

---
# readEntries

## Summary

Read the next block of entries from this directory.

**Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

*Method of [apis/filesystem/DirectoryReader](/apis/filesystem/DirectoryReader)*

## Syntax

``` {.js}
 DirectoryReader.readEntries(successCallback, errorCallback);
```

## Parameters

### successCallback

 Data-typeÂ
:   String

 Called once per successful call to readEntries to deliver the next previously-unreported set of Entries in the associated Directory. If all Entries have already been returned from previous invocations of readEntries, successCallback must be called with a zero-length array as an argument.

### errorCallback

 Data-typeÂ
:   String

*(Optional)*

A callback indicating that there was an error reading from the Directory.

## Return Value

No return value

**Needs Examples**: This section should include examples.

## Related specifications

Specification
:   Status
[W3C File API: Directories and System Specification](http://dev.w3.org/2009/dap/file-system/pub/FileSystem/)
:   W3C Working Draft

