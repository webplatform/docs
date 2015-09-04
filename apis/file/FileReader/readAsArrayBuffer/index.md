---
title: readAsArrayBuffer
tags:
  0: API
  1: Object
  2: Methods
  4: FileAPI
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Returns partial Blob data representing the number of bytes currently loaded (as a fraction of the total), as an ArrayBuffer object, a fixed-length binary data buffer.'
uri: apis/file/FileReader/readAsArrayBuffer

---
# readAsArrayBuffer

## Summary

Returns partial Blob data representing the number of bytes currently loaded (as a fraction of the total), as an ArrayBuffer object, a fixed-length binary data buffer.

*Method of [apis/file/FileReader](/apis/file/FileReader)*

## Syntax

``` {.js}
var  = FileReader.readAsArrayBuffer(blob);
```

## Parameters

### blob

 Data-typeÂ
:   Blob

## Return Value

Returns an object of type DOM Node.

Type: **HRESULT**

This method can return one of these values.

S\_OK

## Examples

``` {.js}
var reader = new FileReader();

reader.onload = function(e) {
  var arrayBuffer = reader.result;
}

reader.readAsArrayBuffer(file);
```

## Notes

This method asynchronously starts reading the contents of the specified File. When the read operation is finished, `readyState` will become `DONE` and the `onloadend` event handler (that is, callback), if present, will be invoked. At that time, the `result` attribute contains an array buffer object representing the file's data.

## Related specifications

Specification
:   Status
[W3C File API Specification](http://www.w3.org/TR/FileAPI)
:   W3C Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

