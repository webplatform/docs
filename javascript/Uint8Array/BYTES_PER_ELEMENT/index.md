---
title: 'BYTES PER ELEMENT'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer JavaScript reference Article](http://msdn.microsoft.com/en-us/library/ie/yek4tbz0%28v=vs.94%29.aspx)'
compatibility:
  feature: 'BYTES PER ELEMENT'
  topic: javascript
readiness: 'Ready to Use'
summary: 'The size in bytes of each element in the array.'
tags:
  - JS_Basic
uri: 'javascript/Uint8Array/BYTES PER ELEMENT'

---
## Summary

The size in bytes of each element in the array.

## Syntax

    var arraySize = int8Array.BYTES_PER_ELEMENT;

## Examples

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
             var intArr = new Uint8Array(buffer.byteLength);
             alert(intArr.BYTES_PER_ELEMENT);
         }
     }
```

