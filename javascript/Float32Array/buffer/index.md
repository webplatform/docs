---
title: buffer
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/br212905(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Read-only. Gets the ArrayBuffer that is referenced by this array.'
tags:
  - JS
  - Basic
uri: javascript/Float32Array/buffer

---
## <span>Summary</span>

Read-only. Gets the ArrayBuffer that is referenced by this array.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    var arrayBuffer = float32Array.buffer;

## <span>Examples</span>

The following example shows how to get the ArrayBuffer of the array.

``` js
var req = new XMLHttpRequest();
     req.open('GET', "http://www.example.com");
     req.responseType = "arraybuffer";
     req.send();

     req.onreadystatechange = function () {
         if (req.readyState === 4) {
             var buffer = req.response;
             var dataView = new DataView(buffer);
             var floatArr = new Float32Array(buffer.byteLength / 4);
             alert(floatArr.buffer.byteLength);
         }
     }
```

