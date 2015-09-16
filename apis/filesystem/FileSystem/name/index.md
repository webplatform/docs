---
title: name
notes:
  - 'Out of date; feature discontinued. See http://www.w3.org/TR/file-system-api/.'
readiness: 'Out of Date'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/filesystem/FileSystem
    href: /apis/filesystem/FileSystem
  return:
    predicate: 'Returns an object of type '
    value: ''
    href: /apis/filesystem/FileSystem
standardization_status: 'W3C Working Draft'
summary: "The name of the file system. The specifics of naming filesystems is unspecified, but a name must be unique across the list of exposed file systems.\n"
tags:
  0: API
  1: Object
  2: Properties
  4: FileSystemAPI
uri: apis/filesystem/FileSystem/name

---
## Summary

The name of the file system. The specifics of naming filesystems is unspecified, but a name must be unique across the list of exposed file systems.

**Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

Property of [apis/filesystem/FileSystem](/apis/filesystem/FileSystem)[apis/filesystem/FileSystem](/apis/filesystem/FileSystem)

## Syntax

**Note**: This property is read-only.

``` js
var result = FileSystem.name;
```

## Return Value

Returns an object of type

DOMString

**Needs Examples**: This section should include examples.

## Related specifications

[W3C File API: Directories and System Specification](http://dev.w3.org/2009/dap/file-system/pub/FileSystem/)
:   W3C Working Draft
