---
title: length
tags:
  - JS
  - Basic
readiness: 'Ready to Use'
summary: 'The length of the array.'
uri: javascript/Int8Array/length

---
# length

## Summary

The length of the array.

## Syntax

    var arrayLength = int8Array.length;

## Examples

The following example shows how to get the length of the array.

``` {.js}
var req = new XMLHttpRequest();
     req.open('GET', "http://www.example.com");
     req.responseType = "arraybuffer";
     req.send();

     req.onreadystatechange = function () {
         if (req.readyState === 4) {
             var buffer = req.response;
             var dataView = new DataView(buffer);
             var intArr = new Int8Array(buffer.byteLength);
             alert(intArr.length);
         }
     }
```

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/br230744(v=vs.94).aspx)

