---
title: moveTo
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
## <span>Summary</span>

Move an Entry to a different location on the file system.

**Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

Method of [apis/filesystem/Entry](/apis/filesystem/Entry)[apis/filesystem/Entry](/apis/filesystem/Entry)

## <span>Syntax</span>

``` js
 Entry.moveTo(parent, newName);
```

## <span>Parameters</span>

### <span>parent</span>

 Data-type
:   String

 The directory to which to move the Entry.

### <span>newName</span>

 Data-type
:   String

(Optional)

The new name of the Entry. Defaults to the Entry's current name if unspecified.

### <span>successCallback</span>

 Data-type
:   String

(Optional)

A callback that is called with the Entry for the new location.

### <span>errorCallback</span>

 Data-type
:   String

(Optional)

A callback that is called when errors happen.

## <span>Return Value</span>

No return value

**Needs Examples**: This section should include examples.

## <span>Notes</span>

It is an error to try to:

-   move a directory inside itself or to any child at any depth;
-   move an Entry into its parent if a name different from its current one isn't provided;
-   move a file to a path occupied by a directory;
-   move a directory to a path occupied by a file;
-   move any element to a path occupied by a directory which is not empty.

A move of a file on top of an existing file must attempt to delete and replace that file.

A move of a directory on top of an existing empty directory must attempt to delete and replace that directory.

## <span>Related specifications</span>

[W3C File API: Directories and System Specification](http://dev.w3.org/2009/dap/file-system/pub/FileSystem/)
:   W3C Working Draft
