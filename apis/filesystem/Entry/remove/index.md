---
title: remove
tags:
  0: API
  1: Object
  2: Methods
  4: FileSystemAPI
readiness: 'Out of Date'
standardization_status: 'W3C Working Draft'
notes:
  - 'Out of date; feature discontinued. See http://www.w3.org/TR/file-system-api/.'
summary: "Deletes a file or directory.\n"
uri: apis/filesystem/Entry/remove

---
# remove

## Summary

Deletes a file or directory.

**Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

*Method of [apis/filesystem/Entry](/apis/filesystem/Entry)*

## Syntax

``` {.js}
 Entry.remove(successCallback, errorCallback);
```

## Parameters

### successCallback

 Data-typeÂ
:   String

 A callback that is called on success.

### errorCallback

 Data-typeÂ
:   String

*(Optional)*

A callback that is called when errors happen.

## Return Value

No return value

**Needs Examples**: This section should include examples.

## Notes

It is an error to attempt to delete a directory that is not empty.

It is an error to attempt to delete the root directory of a filesystem.

## Related specifications

Specification
:   Status
[W3C File API: Directories and System Specification](http://dev.w3.org/2009/dap/file-system/pub/FileSystem/)
:   W3C Working Draft

