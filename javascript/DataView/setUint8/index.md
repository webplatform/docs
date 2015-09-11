---
title: setUint8
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/br212478(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Stores a Uint8 value at the specified byte offset from the start of the view.'
tags:
  - JS
  - Basic
uri: javascript/DataView/setUint8

---
## <span>Summary</span>

Stores a Uint8 value at the specified byte offset from the start of the view.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    dataView.setUint8(byteOffset, value);

**byteOffset**
:   The place in the buffer at which the value should be set.

**value**
:   The value to set.

## <span>Examples</span>

The following example shows how to set the first Uint8 in the DataView.

``` js
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

## <span>Remarks</span>

These methods raise an exception if they would write beyond the end of the view.

