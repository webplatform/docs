---
title: 'byteLength'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/br212935(v=vs.94).aspx)'
compatibility:
  feature: byteLength
  topic: javascript
readiness: 'Ready to Use'
summary: 'Read-only. The length of this array from the start of its ArrayBuffer, in bytes, as fixed at construction time.'
tags:
  - JS
  - Basic
uri: javascript/Float64Array/byteLength

---
## Summary

Read-only. The length of this array from the start of its ArrayBuffer, in bytes, as fixed at construction time.

## Syntax

    var arrayByteLength = float64Array.byteLength;

## Examples

The following example shows how to get the byte length of the array.

``` js
var req = new XMLHttpRequest();
     req.open('GET', "http://www.example.com");
     req.responseType = "arraybuffer";
     req.send();

     req.onreadystatechange = function () {
         if (req.readyState === 4) {
             var buffer = req.response;
             var dataView = new DataView(buffer);
             var floatArr = new Float64Array(buffer.byteLength / 8);
             alert(floatArr.byteLength);
         }
     }
```

