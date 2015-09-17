---
title: 'length'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/br230729(v=vs.94).aspx)'
compatibility:
  feature: length
  topic: javascript
readiness: 'Ready to Use'
summary: 'The length of the array.'
tags:
  - JS_Basic
uri: javascript/Float32Array/length

---
## Summary

The length of the array.

## Syntax

    var arrayLength = float32Array.length;

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
             var floatArr = new Float32Array(buffer.byteLength / 4);
             alert(floatArr.length);
         }
     }
```

