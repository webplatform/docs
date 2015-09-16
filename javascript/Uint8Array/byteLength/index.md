---
title: 'byteLength'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer JavaScript reference Article](http://msdn.microsoft.com/en-us/library/ie/yek4tbz0%28v=vs.94%29.aspx)'
compatibility:
  feature: byteLength
  topic: javascript
readiness: 'Ready to Use'
summary: 'Read-only. The length of this array from the start of its ArrayBuffer, in bytes, as fixed at construction time.'
tags:
  - JS
  - Basic
uri: javascript/Uint8Array/byteLength

---
## Summary

Read-only. The length of this array from the start of its ArrayBuffer, in bytes, as fixed at construction time.

## Syntax

    var arrayByteLength = uint8Array.byteLength;

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
             var intArr = new Uint8Array(buffer.byteLength);
             alert(intArr.byteLength);
         }
     }
```

