---
title: BYTES PER ELEMENT
tags:
  - JS
  - Basic
readiness: 'Ready to Use'
summary: 'The size in bytes of each element in the array.'
uri: 'javascript/Float64Array/BYTES PER ELEMENT'

---
# BYTES PER ELEMENT

## Summary

The size in bytes of each element in the array.

## Syntax

    var arraySize = int8Array.BYTES_PER_ELEMENT;

## Examples

The following example shows how to get the size of the array elements.

``` {.js}
var req = new XMLHttpRequest();
     req.open('GET', "http://www.example.com");
     req.responseType = "arraybuffer";
     req.send();

     req.onreadystatechange = function () {
         if (req.readyState === 4) {
             var buffer = req.response;
             var dataView = new DataView(buffer);
             var floatArr = new Float64Array(buffer.byteLength / 8);
             alert(floatArr.BYTES_PER_ELEMENT);
         }
     }
```

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/br230742(v=vs.94).aspx)

