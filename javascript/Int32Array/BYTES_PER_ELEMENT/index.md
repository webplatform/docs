---
title: BYTES PER ELEMENT
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/br230722(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'The size in bytes of each element in the array.'
tags:
  - JS
  - Basic
uri: 'javascript/Int32Array/BYTES PER ELEMENT'

---
## <span>Summary</span>

The size in bytes of each element in the array.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    var arraySize = int8Array.BYTES_PER_ELEMENT;

## <span>Examples</span>

The following example shows how to get the size of the array elements.

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
             alert(intArr.BYTES_PER_ELEMENT);
         }
     }
```

