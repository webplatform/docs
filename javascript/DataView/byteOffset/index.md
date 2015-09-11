---
title: byteOffset
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/br212912(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Read-only. The offset of this view from the start of its ArrayBuffer, in bytes, as fixed at construction time.'
tags:
  - JS
  - Basic
uri: javascript/DataView/byteOffset

---
## <span>Summary</span>

Read-only. The offset of this view from the start of its ArrayBuffer, in bytes, as fixed at construction time.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    var arrayOffset = dataView.byteOffset;

## <span>Examples</span>

The following example shows how to get the length of a DataView.

``` js
var req = new XMLHttpRequest();
     req.open('GET', "http://www.example.com");
     req.responseType = "arraybuffer";
     req.send();

     req.onreadystatechange = function () {
         if (req.readyState === 4) {
             var buffer = req.response;
             var dataView = new DataView(buffer);
             alert(dataView.byteOffset)
         }
     }
```

