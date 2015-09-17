---
title: 'response'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest/Sending_and_Receiving_Binary_Data)'
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/xhr/XMLHttpRequest
    href: /apis/xhr/XMLHttpRequest
  return:
    predicate: 'Returns an object of type '
    value: any
    href: /apis/xhr/XMLHttpRequest
standardization_status: 'W3C Working Draft'
summary: 'Returns the response entity body, which is the fragment of the entity body of the response received so far (if LOADING) or the complete entity body of the response (if DONE).'
tags:
  - API_Object_Properties
  - API
  - XHR
uri: apis/xhr/XMLHttpRequest/response

---
## Summary

Returns the response entity body, which is the fragment of the entity body of the response received so far (if LOADING) or the complete entity body of the response (if DONE).

Property of [apis/xhr/XMLHttpRequest](/apis/xhr/XMLHttpRequest)[apis/xhr/XMLHttpRequest](/apis/xhr/XMLHttpRequest)

## Syntax

**Note**: This property is read-only.

``` js
var result = element.response;
```

## Return Value

Returns an object of type anyany

## Examples

This example reads an image as a binary file and creates an 8-bit unsigned integer array from the raw bytes.

``` js
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

[W3C XMLHttpRequest Specification](http://www.w3.org/TR/XMLHttpRequest/)
:   W3C Working Draft
