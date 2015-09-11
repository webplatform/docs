---
title: length
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer JavaScript reference Article](http://msdn.microsoft.com/en-us/library/ie/yek4tbz0%28v=vs.94%29.aspx)'
readiness: 'Ready to Use'
summary: 'The length of the array.'
tags:
  - JS
  - Basic
uri: javascript/Uint32Array/length

---
## <span>Summary</span>

The length of the array.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    var arrayLength = uint32Array.length;

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
             var intArr = new Uint32Array(buffer.byteLength / 4);
             alert(intArr.length);
         }
     }
```

