---
title: byteLength
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/br212926(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Read-only. The length of this view from the start of its ArrayBuffer, in bytes, as fixed at construction time.'
tags:
  - JS
  - Basic
uri: javascript/DataView/byteLength

---
## Summary

Read-only. The length of this view from the start of its ArrayBuffer, in bytes, as fixed at construction time.

## Syntax

<span class="language">JavaScript</span>

    var byteLength = dataView.byteLength;

## Examples

The following example shows how get the length of a DataView from an XMLHttpRequest.

``` js
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

