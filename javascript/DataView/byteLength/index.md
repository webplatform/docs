---
title: byteLength
tags:
  - JS
  - Basic
readiness: 'Ready to Use'
summary: 'Read-only. The length of this view from the start of its ArrayBuffer, in bytes, as fixed at construction time.'
uri: javascript/DataView/byteLength

---
# byteLength

## Summary

Read-only. The length of this view from the start of its ArrayBuffer, in bytes, as fixed at construction time.

## Syntax

    var byteLength = dataView.byteLength;

## Examples

The following example shows how get the length of a DataView from an XMLHttpRequest.

``` {.js}
var req = new XMLHttpRequest();
     req.open('GET', "http://www.example.com");
     req.responseType = "arraybuffer";
     req.send();

     req.onreadystatechange = function () {
         if (req.readyState === 4) {
             var buffer = req.response;
             var dataView = dataView.buffer;
             alert(dataView.byteLength);
         }
     }
```

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/br212926(v=vs.94).aspx)

