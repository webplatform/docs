---
title: toURL
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
  0: API
  1: Object
  2: Methods
  4: FileSystemAPI
uri: apis/filesystem/EntrySync/toURL

---
## <span>Summary</span>

Returns a URL that can be used to identify this EntrySync.

**Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

Method of [apis/filesystem/EntrySync](/apis/filesystem/EntrySync)[apis/filesystem/EntrySync](/apis/filesystem/EntrySync)

## <span>Syntax</span>

``` js
var  = EntrySync.toURL();
```

## <span>Return Value</span>

Returns an object of type<span></span>

DOMString

**Needs Examples**: This section should include examples.

## <span>Notes</span>

The URL has no specific expiration; as it describes a location on disk, it should be valid at least as long as that location exists.

## <span>Related specifications</span>

[W3C File API: Directories and System Specification](http://dev.w3.org/2009/dap/file-system/pub/FileSystem/)
:   W3C Working Draft
