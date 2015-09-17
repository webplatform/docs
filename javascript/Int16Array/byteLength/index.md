---
title: 'byteLength'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/br230748(v=vs.94).aspx)'
compatibility:
  feature: byteLength
  topic: javascript
readiness: 'Ready to Use'
summary: 'Read-only. The length of this array from the start of its ArrayBuffer, in bytes, as fixed at construction time.'
tags:
  - JS_Basic
uri: javascript/Int16Array/byteLength

---
## Summary

Read-only. The length of this array from the start of its ArrayBuffer, in bytes, as fixed at construction time.

## Syntax

    var arrayByteLength = int16Array.byteLength;

## Examples

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
             var intArr = new Int16Array(buffer.byteLength / 2);
             alert(intArr.byteLength);
         }
     }
```

