---
title: 'getInt8'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/br212471(v=vs.94).aspx)'
compatibility:
  feature: getInt8
  topic: javascript
readiness: 'Ready to Use'
summary: 'Gets the Int8 value at the specified byte offset from the start of the view. There is no alignment constraint; multi-byte values may be fetched from any offset.'
tags:
  - JS_Basic
uri: javascript/DataView/getInt8

---
## Summary

Gets the Int8 value at the specified byte offset from the start of the view. There is no alignment constraint; multi-byte values may be fetched from any offset.

## Syntax

    var testInt = dataView.getInt8(byteOffset);

**testInt**
:   Required. The Int8 value that is returned from the method.

**byteOffset**
:   The place in the buffer at which the value should be retrieved.

## Examples

The following example shows how to get the first Int8 in the DataView.

``` js
var req = new XMLHttpRequest();
     req.open('GET', "http://www.example.com");
     req.responseType = "arraybuffer";
     req.send();

     req.onreadystatechange = function () {
         if (req.readyState === 4) {
             var buffer = req.response;
             var dataView = new DataView(buffer);
             alert(dataView.getInt8(0));
         }
     }
```

## Remarks

These methods raise an exception if they would read beyond the end of the view.

