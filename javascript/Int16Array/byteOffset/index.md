---
title: 'byteOffset'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/br212913(v=vs.94).aspx)'
compatibility:
  feature: byteOffset
  topic: javascript
readiness: 'Ready to Use'
summary: 'Read-only. The offset of this array from the start of its ArrayBuffer, in bytes, as fixed at construction time.'
tags:
  - JS
  - Basic
uri: javascript/Int16Array/byteOffset

---
## Summary

Read-only. The offset of this array from the start of its ArrayBuffer, in bytes, as fixed at construction time.

## Syntax

    var arrayOffset = int16Array.byteOffset;

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
             var intArr = new Int16Array(buffer.byteLength / 2);
             alert(intArr.byteOffset);
         }
     }
```

