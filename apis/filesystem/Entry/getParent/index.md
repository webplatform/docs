---
title: getParent
tags:
  0: API
  1: Object
  2: Methods
  4: FileSystemAPI
readiness: 'Out of Date'
standardization_status: 'W3C Working Draft'
notes:
  - 'Out of date; feature discontinued. See http://www.w3.org/TR/file-system-api/.'
summary: "Look up the parent DirectoryEntry containing this Entry. If this Entry is the root of its filesystem, its parent is itself.\n"
uri: apis/filesystem/Entry/getParent

---
# getParent

## Summary

Look up the parent DirectoryEntry containing this Entry. If this Entry is the root of its filesystem, its parent is itself.

**Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

*Method of [apis/filesystem/Entry](/apis/filesystem/Entry)*

## Syntax

``` {.js}
 Entry.getParent(successCallback, errorCallback);
```

## Parameters

### successCallback

 Data-typeÂ
:   String

 A callback that is called to return the parent Entry.

### errorCallback

 Data-typeÂ
:   String

*(Optional)*

A callback that is called when errors happen.

## Return Value

No return value

**Needs Examples**: This section should include examples.

## Related specifications

Specification
:   Status
[W3C File API: Directories and System Specification](http://dev.w3.org/2009/dap/file-system/pub/FileSystem/)
:   W3C Working Draft

