---
title: responseType
tags:
  0: API
  1: Object
  2: Properties
  4: XHR
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Returns or sets the format the response will be returned in.'
uri: apis/xhr/XMLHttpRequest/responseType

---
# responseType

## Summary

Returns or sets the format the response will be returned in.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/xhr/XMLHttpRequest](/apis/xhr/XMLHttpRequest)</span></span>

## Syntax

``` {.js}
var result = element.responseType;
element.responseType = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value"></span></span>

XMLHttpRequestResponseType, which is one of the following:

-   "arraybuffer": an ArrayBuffer
-   "blob": a Blob
-   "document": a Document
-   "json": a JavaScript object, parsed from a JSON string returned by the server
-   "text": a String

## Examples

The following code demonstrates to how to use the requestType property of the **XMLHttpRequest** object to retrieve the results of the XHR request as an **ArrayBuffer**.

This can be used to load images, audio and other binary data with an XHR request. Once the response is received use the **response** property to access the ArrayBuffer.

``` {.js}
function handler() {
  if (xhr.readyState === 4 /* complete */) {
    if (xhr.status === 200) {
            console.log(xhr.response);
        }
    }
}
var xhr = new XMLHttpRequest();
xhr.responseType = "arraybuffer";
xhr.open("GET", "http://localhost/test.ogg", true);
xhr.onreadystatechange = handler;
xhr.send();
```

## Related specifications

Specification
:   Status
[W3C XMLHttpRequest Specification](http://www.w3.org/TR/XMLHttpRequest/)
:   W3C Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

