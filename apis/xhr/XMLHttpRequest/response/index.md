---
title: response
tags:
  0: API
  1: Object
  2: Properties
  4: XHR
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Returns the response entity body, which is the fragment of the entity body of the response received so far (if LOADING) or the complete entity body of the response (if DONE).'
uri: apis/xhr/XMLHttpRequest/response

---
# response

## Summary

Returns the response entity body, which is the fragment of the entity body of the response received so far (if LOADING) or the complete entity body of the response (if DONE).

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/xhr/XMLHttpRequest](/apis/xhr/XMLHttpRequest)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = element.response;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">any</span></span>

## Examples

This example reads an image as a binary file and creates an 8-bit unsigned integer array from the raw bytes.

``` {.js}
var oReq = new XMLHttpRequest();
oReq.open("GET", "/myfile.png", true);
oReq.responseType = "arraybuffer";

oReq.onload = function (oEvent) {
  var arrayBuffer = oReq.response; // Note: not oReq.responseText
  if (arrayBuffer) {
    var byteArray = new Uint8Array(arrayBuffer);
    for (var i = 0; i < byteArray.byteLength; i++) {
      // do something with each byte in the array
    }
  }
};

oReq.send(null);
```

## Related specifications

Specification
:   Status
[W3C XMLHttpRequest Specification](http://www.w3.org/TR/XMLHttpRequest/)
:   W3C Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest/Sending_and_Receiving_Binary_Data)

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

