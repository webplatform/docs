---
title: length
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/br230744(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'The length of the array.'
tags:
  - JS
  - Basic
uri: javascript/Int8Array/length

---
## <span>Summary</span>

The length of the array.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    var arrayLength = int8Array.length;

## <span>Examples</span>

The following example shows how to get the length of the array.

``` js
var req = new XMLHttpRequest();
     req.open('GET', "http://www.example.com");
     req.responseType = "arraybuffer";
     req.send();

     req.onreadystatechange = function () {
         if (req.readyState === 4) {
             var buffer = req.response;
             var dataView = new DataView(buffer);
             var intArr = new Int8Array(buffer.byteLength);
             alert(intArr.length);
         }
     }
```

