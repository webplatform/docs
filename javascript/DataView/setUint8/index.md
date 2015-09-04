---
title: setUint8
tags:
  - JS
  - Basic
readiness: 'Ready to Use'
summary: 'Stores a Uint8 value at the specified byte offset from the start of the view.'
uri: javascript/DataView/setUint8

---
# setUint8

## Summary

Stores a Uint8 value at the specified byte offset from the start of the view.

## Syntax

    dataView.setUint8(byteOffset, value);

**byteOffset**
:   The place in the buffer at which the value should be set.

**value**
:   The value to set.

## Examples

The following example shows how to set the first Uint8 in the DataView.

``` {.js}
var req = new XMLHttpRequest();
     req.open('GET', "http://www.example.com");
     req.responseType = "arraybuffer";
     req.send();

     req.onreadystatechange = function () {
         if (req.readyState === 4) {
             var buffer = req.response;
             var dataView = new DataView(buffer);
             dataView.setUint8(0, 9);
         }
     }
```

## Remarks

These methods raise an exception if they would write beyond the end of the view.

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/br212478(v=vs.94).aspx)

