---
title: getMetadata
notes:
  - 'Out of date; feature discontinued. See http://www.w3.org/TR/file-system-api/.'
readiness: 'Out of Date'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/filesystem/Entry
    href: /apis/filesystem/Entry
standardization_status: 'W3C Working Draft'
summary: "Look up metadata about this Entry.\n"
tags:
  0: API
  1: Object
  2: Methods
  4: FileSystemAPI
uri: apis/filesystem/Entry/getMetadata

---
## <span>Summary</span>

Look up metadata about this Entry.

**Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

Method of [apis/filesystem/Entry](/apis/filesystem/Entry)[apis/filesystem/Entry](/apis/filesystem/Entry)

## <span>Syntax</span>

``` js
 Entry.getMetadata(successCallback, errorCallback);
```

## <span>Parameters</span>

### <span>successCallback</span>

 Data-type
:   String

 A callback that is called with the time of the last modification.

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
