---
title: 'moveTo'
notes:
  - 'Out of date; feature discontinued. See http://www.w3.org/TR/file-system-api/.'
readiness: 'Out of Date'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/filesystem/Entry
    href: /apis/filesystem/Entry
standardization_status: 'W3C Working Draft'
summary: "Move an Entry to a different location on the file system.\n"
tags:
  0: API
  1: Object
  2: Methods
  4: FileSystemAPI
uri: apis/filesystem/Entry/moveTo

---
## Summary

Move an Entry to a different location on the file system.

**Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

Method of [apis/filesystem/Entry](/apis/filesystem/Entry)[apis/filesystem/Entry](/apis/filesystem/Entry)

## Syntax

``` js
 Entry.moveTo(parent, newName);
```

## Parameters

### parent

 Data-type
:   String

 The directory to which to move the Entry.

### newName

 Data-type
:   String

(Optional)

The new name of the Entry. Defaults to the Entry's current name if unspecified.

### successCallback

 Data-type
:   String

(Optional)

A callback that is called with the Entry for the new location.

### errorCallback

 Data-type
:   String

(Optional)

A callback that is called when errors happen.

## Return Value

No return value

**Needs Examples**: This section should include examples.

## Notes

It is an error to try to:

-   move a directory inside itself or to any child at any depth;
-   move an Entry into its parent if a name different from its current one isn't provided;
-   move a file to a path occupied by a directory;
-   move a directory to a path occupied by a file;
-   move any element to a path occupied by a directory which is not empty.

A move of a file on top of an existing file must attempt to delete and replace that file.

A move of a directory on top of an existing empty directory must attempt to delete and replace that directory.

## Related specifications

[W3C File API: Directories and System Specification](http://dev.w3.org/2009/dap/file-system/pub/FileSystem/)
:   W3C Working Draft
