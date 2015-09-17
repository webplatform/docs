---
title: 'toURL'
notes:
  - 'Out of date; feature discontinued. See http://www.w3.org/TR/file-system-api/.'
readiness: 'Out of Date'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/filesystem/EntrySync
    href: /apis/filesystem/EntrySync
  return_type:
    predicate: 'Returns an object of type  '
    value: ''
    href: /apis/filesystem/EntrySync
standardization_status: 'W3C Working Draft'
summary: "Returns a URL that can be used to identify this EntrySync.\n"
tags:
  - API_Object_Methods
  - API
  - FileSystemAPI
  - Needs_Examples
uri: apis/filesystem/EntrySync/toURL

---
## Summary

Returns a URL that can be used to identify this EntrySync.

**Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

Method of [apis/filesystem/EntrySync](/apis/filesystem/EntrySync)[apis/filesystem/EntrySync](/apis/filesystem/EntrySync)

## Syntax

``` js
var  = EntrySync.toURL();
```

## Return Value

Returns an object of type

DOMString

## Notes

The URL has no specific expiration; as it describes a location on disk, it should be valid at least as long as that location exists.

## Related specifications

[W3C File API: Directories and System Specification](http://dev.w3.org/2009/dap/file-system/pub/FileSystem/)
:   W3C Working Draft
