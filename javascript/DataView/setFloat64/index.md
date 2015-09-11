---
title: setFloat64
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/br212469(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Sets the Float64 value at the specified byte offset from the start of the view. There is no alignment constraint; multi-byte values may be set at any offset.'
tags:
  - JS
  - Basic
uri: javascript/DataView/setFloat64

---
## <span>Summary</span>

Sets the Float64 value at the specified byte offset from the start of the view. There is no alignment constraint; multi-byte values may be set at any offset.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    dataView.setFloat64 (byteOffset, value, littleEndian);

**byteOffset**
:   The place in the buffer at which the value should be retrieved.

**value**
:   The value to set.

**littleEndian**
:   Optional. If false or undefined, a big-endian value should be written, otherwise a little-endian value should be written.

## <span>Examples</span>

The following example shows how to set the first Float64 in the DataView.

``` js
var req = new XMLHttpRequest();
     req.open('GET', "http://www.example.com");
     req.responseType = "arraybuffer";
     req.send();

     req.onreadystatechange = function () {
         if (req.readyState === 4) {
             var buffer = req.response;
             var dataView = new DataView(buffer);
             dataView.setFloat64(0, 9.1);
         }
     }
```

## <span>Remarks</span>

These methods raise an exception if they would write beyond the end of the view.

