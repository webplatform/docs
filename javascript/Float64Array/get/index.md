---
title: 'get'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/br230740(v=vs.94).aspx)'
compatibility:
  feature: get
  topic: javascript
readiness: 'Ready to Use'
summary: 'Omittable. Gets the element at the specified index.'
tags:
  - JS_Basic
uri: javascript/Float64Array/get

---
## Summary

Omittable. Gets the element at the specified index.

## Syntax

    var value = float64Array.get(index);

**value**
:   The value returned by this method.

**index**
:   The index at which to get the element of the array.

## Examples

The following example shows how to get the first element of the array.

``` js
var req = new XMLHttpRequest();
     req.open('GET', "http://www.example.com");
     req.responseType = "arraybuffer";
     req.send();

     req.onreadystatechange = function () {
         if (req.readyState === 4) {
             var buffer = req.response;
             var dataView = new DataView(buffer);
             var floatArr = new Float64Array(buffer.byteLength / 4);
             var element = floatArr.get(0);
         }
     }
```

