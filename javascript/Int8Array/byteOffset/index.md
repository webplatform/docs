---
title: byteOffset
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/br230731(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Read-only. The offset of this array from the start of its ArrayBuffer, in bytes, as fixed at construction time.'
tags:
  - JS
  - Basic
uri: javascript/Int8Array/byteOffset

---
## Summary

Read-only. The offset of this array from the start of its ArrayBuffer, in bytes, as fixed at construction time.

## Syntax

<span class="language">JavaScript</span>

    var arrayOffset = int8Array.byteOffset;

## Examples

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
             var intArr = new Int8Array(buffer.byteLength);
             alert(intArr.byteOffset);
         }
     }
```

