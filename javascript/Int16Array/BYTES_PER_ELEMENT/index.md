---
title: 'BYTES PER ELEMENT'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/br230730(v=vs.94).aspx)'
compatibility:
  feature: 'BYTES PER ELEMENT'
  topic: javascript
readiness: 'Ready to Use'
summary: 'The size in bytes of each element in the array.'
tags:
  - JS_Basic
uri: 'javascript/Int16Array/BYTES PER ELEMENT'

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
             var intArr = new Int16Array(buffer.byteLength / 2);
             alert(intArr.BYTES_PER_ELEMENT);
         }
     }
```

