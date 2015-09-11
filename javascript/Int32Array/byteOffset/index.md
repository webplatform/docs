---
title: byteOffset
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/br212901(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Read-only. The offset of this array from the start of its ArrayBuffer, in bytes, as fixed at construction time.'
tags:
  - JS
  - Basic
uri: javascript/Int32Array/byteOffset

---
## <span>Summary</span>

Read-only. The offset of this array from the start of its ArrayBuffer, in bytes, as fixed at construction time.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    var arrayOffset = int32Array.byteOffset;

## <span>Examples</span>

The following example shows how to get the offset of the array.

``` js
var req = new XMLHttpRequest();
     req.open('GET', "http://www.example.com");
     req.responseType = "arraybuffer";
     req.send();

     req.onreadystatechange = function () {
         if (req.readyState === 4) {
             var buffer = req.response;
             var dataView = new DataView(buffer);
             var intArr = new Int32Array(buffer.byteLength / 4);
             alert(intArr.byteOffset);
         }
     }
```

