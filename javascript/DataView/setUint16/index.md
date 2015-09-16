---
title: setUint16
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/br212481(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Sets the Uint16 value at the specified byte offset from the start of the view. There is no alignment constraint; multi-byte values may be set at any offset.'
tags:
  - JS
  - Basic
uri: javascript/DataView/setUint16

---
## Summary

Sets the Uint16 value at the specified byte offset from the start of the view. There is no alignment constraint; multi-byte values may be set at any offset.

## Syntax

<span class="language">JavaScript</span>

    dataView.setUint16(byteOffset, value, littleEndian);

**testInt**
:   Required. The Uint16 value that is returned from the method.

**value**
:   The value to set.

**byteOffset**
:   The place in the buffer at which the value should be retrieved.

**littleEndian**
:   Optional. If false or undefined, a big-endian value should be written, otherwise a little-endian value should be written.

## Examples

The following example shows how to set the first Uint16 in the DataView.

``` js
var req = new XMLHttpRequest();
     req.open('GET', "http://www.example.com");
     req.responseType = "arraybuffer";
     req.send();

     req.onreadystatechange = function () {
         if (req.readyState === 4) {
             var buffer = req.response;
             var dataView = new DataView(buffer);
             dataView.setUint16(0, 9);
         }
     }
```

## Remarks

These methods raise an exception if they would write beyond the end of the view.

