---
title: byteLength
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/br212482(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Read-only. The length of the ArrayBuffer (in bytes).'
tags:
  - JS
  - Basic
uri: javascript/ArrayBuffer/byteLength

---
## <span>Summary</span>

Read-only. The length of the ArrayBuffer (in bytes).

## <span>Syntax</span>

<span class="language">JavaScript</span>

    var arrayLength = arrayBuffer.byteLength;

## <span>Examples</span>

The following example shows how to get the byte length of the ArrayBuffer.

``` js
var req = new XMLHttpRequest();
     req.open('GET', "http://www.example.com");
     req.responseType = "arraybuffer";
     req.send();

     req.onreadystatechange = function () {
         if (req.readyState === 4) {
             var buffer = req.response;

         alert(buffer.byteLength);
         }
     }
```

