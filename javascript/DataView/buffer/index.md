---
title: 'buffer'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/br230733(v=vs.94).aspx)'
compatibility:
  feature: buffer
  topic: javascript
readiness: 'Ready to Use'
summary: 'Read-only. Gets the ArrayBuffer that is referenced by this view.'
tags:
  - JS
  - Basic
uri: javascript/DataView/buffer

---
## Summary

Read-only. Gets the ArrayBuffer that is referenced by this view.

## Syntax

    var arrayBuffer = dataView.buffer;

## Examples

The following example shows how to get the length of the ArrayBuffer underlying the DataView.

``` js
var req = new XMLHttpRequest();
     req.open('GET', "http://www.example.com");
     req.responseType = "arraybuffer";
     req.send();

     req.onreadystatechange = function () {
         if (req.readyState === 4) {
             var buffer = req.response;
             var dataView = new DataView(buffer);
             alert(dataView.buffer.byteLength)
         }
     }
```

