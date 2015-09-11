---
title: getUint16
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/br212467(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Gets the Uint16 value at the specified byte offset from the start of the view. There is no alignment constraint; multi-byte values may be fetched from any offset.'
tags:
  - JS
  - Basic
uri: javascript/DataView/getUint16

---
## <span>Summary</span>

Gets the Uint16 value at the specified byte offset from the start of the view. There is no alignment constraint; multi-byte values may be fetched from any offset.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    var testInt = dataView.getUint16(byteOffset, littleEndian);

**testInt**
:   Required. The Uint16 value that is returned from the method.

**byteOffset**
:   The place in the buffer at which the value should be retrieved.

**littleEndian**
:   Optional. If false or undefined, a big-endian value should be read, otherwise a little-endian value should be read.

## <span>Examples</span>

The following example shows how to get the first Uint16 in the DataView.

``` js
var req = new XMLHttpRequest();
     req.open('GET', "http://www.example.com");
     req.responseType = "arraybuffer";
     req.send();

     req.onreadystatechange = function () {
         if (req.readyState === 4) {
             var buffer = req.response;
             var dataView = new DataView(buffer);
             alert(dataView.getUint16(0));
         }
     }
```

## <span>Remarks</span>

These methods raise an exception if they would read beyond the end of the view.

