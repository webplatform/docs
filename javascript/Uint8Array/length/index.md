---
title: 'length'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer JavaScript reference Article](http://msdn.microsoft.com/en-us/library/ie/yek4tbz0%28v=vs.94%29.aspx)'
compatibility:
  feature: length
  topic: javascript
readiness: 'Ready to Use'
summary: 'The length of the array.'
tags:
  - JS_Basic
uri: javascript/Uint8Array/length

---
## Summary

The length of the array.

## Syntax

    var arrayLength = uint8Array.length;

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
             alert(intArr.length);
         }
     }
```

