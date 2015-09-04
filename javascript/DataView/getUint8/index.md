---
title: getUint8
tags:
  - JS
  - Basic
readiness: 'Ready to Use'
summary: 'Gets the Uint8 value at the specified byte offset from the start of the view. There is no alignment constraint; multi-byte values may be fetched from any offset.'
uri: javascript/DataView/getUint8

---
# getUint8

## Summary

Gets the Uint8 value at the specified byte offset from the start of the view. There is no alignment constraint; multi-byte values may be fetched from any offset.

## Syntax

    var testInt = dataView.getUint8(byteOffset);

**testInt**
:   Required. The Uint8 value that is returned from the method.

**byteOffset**
:   The place in the buffer at which the value should be retrieved.

## Examples

The following example shows how to get the first Uint8 in the DataView.

``` {.js}
var req = new XMLHttpRequest();
     req.open('GET', "http://www.example.com");
     req.responseType = "arraybuffer";
     req.send();

     req.onreadystatechange = function () {
         if (req.readyState === 4) {
             var buffer = req.response;
             var dataView = new DataView(buffer);
             alert(dataView.getUint8(0));
         }
     }
```

## Remarks

These methods raise an exception if they would read beyond the end of the view.

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/br212473(v=vs.94).aspx)

