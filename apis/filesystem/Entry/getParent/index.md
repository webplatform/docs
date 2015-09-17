---
title: 'getParent'
notes:
  - 'Out of date; feature discontinued. See http://www.w3.org/TR/file-system-api/.'
readiness: 'Out of Date'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/filesystem/Entry
    href: /apis/filesystem/Entry
standardization_status: 'W3C Working Draft'
summary: "Look up the parent DirectoryEntry containing this Entry. If this Entry is the root of its filesystem, its parent is itself.\n"
tags:
  - API_Object_Methods
  - API
  - FileSystemAPI
  - Needs_Examples
uri: apis/filesystem/Entry/getParent

---
## Summary

Look up the parent DirectoryEntry containing this Entry. If this Entry is the root of its filesystem, its parent is itself.

**Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

Method of [apis/filesystem/Entry](/apis/filesystem/Entry)[apis/filesystem/Entry](/apis/filesystem/Entry)

## Syntax

``` js
 Entry.getParent(successCallback, errorCallback);
```

## Parameters

### successCallback

 Data-type
:   String

 A callback that is called to return the parent Entry.

### errorCallback

 Data-type
:   String

(Optional)

A callback that is called when errors happen.

## Return Value

No return value

## Related specifications

[W3C File API: Directories and System Specification](http://dev.w3.org/2009/dap/file-system/pub/FileSystem/)
:   W3C Working Draft
