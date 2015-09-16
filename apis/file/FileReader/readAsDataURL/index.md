---
title: readAsDataURL
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/file/FileReader
    href: /apis/file/FileReader
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /apis/file/FileReader
standardization_status: 'W3C Working Draft'
summary: 'Returns the complete data of blob as a Data URL, essentially a Base64-encoded string of the file data.'
tags:
  0: API
  1: Object
  2: Methods
  4: FileAPI
uri: apis/file/FileReader/readAsDataURL

---
## Summary

Returns the complete data of blob as a Data URL, essentially a Base64-encoded string of the file data.

Method of [apis/file/FileReader](/apis/file/FileReader)[apis/file/FileReader](/apis/file/FileReader)

## Syntax

``` js
var  = FileReader.readAsDataURL(blob);
```

## Parameters

### blob

 Data-type
:   Blob

 Represents a chunk of immutable raw data.

## Return Value

Returns an object of type DOM NodeDOM Node

Type: **HRESULT**

This method can return one of these values.

S\_OK

## Examples

``` js
var reader = new FileReader();

reader.onload = function(e) {
  var dataURL = reader.result;
}

reader.readAsDataURL(file);
```

## Notes

This method asynchronously starts reading the contents of the specified [**File**](/apis/file/File) or [**Blob**](/apis/file/Blob). When the read operation is complete, `readyState` will become `DONE` and the `onloadend` event handler (that is, callback), if present, will be invoked. At that time, the `result` property contains a data URL string that encodes the file's data.

## Related specifications

[W3C File API Specification](http://www.w3.org/TR/FileAPI)
:   W3C Working Draft
