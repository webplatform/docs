---
title: buffer
tags:
  - JS
  - Basic
readiness: 'Ready to Use'
summary: 'Read-only. Gets the ArrayBuffer that is referenced by this array.'
uri: javascript/Uint32Array/buffer

---
# buffer

## Summary

Read-only. Gets the ArrayBuffer that is referenced by this array.

## Syntax

    var arrayBuffer = uint32Array.buffer;

## Examples

The following example shows how to get the ArrayBuffer of the array.

``` {.js}
var req = new XMLHttpRequest();
     req.open('GET', "http://www.example.com");
     req.responseType = "arraybuffer";
     req.send();

     req.onreadystatechange = function () {
         if (req.readyState === 4) {
             var buffer = req.response;
             var dataView = new DataView(buffer);
             var intArr = new Uint32Array(buffer.byteLength / 4);
             alert(intArr.buffer.byteLength);
         }
     }
```

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer JavaScript reference Article](http://msdn.microsoft.com/en-us/library/ie/yek4tbz0%28v=vs.94%29.aspx)

