---
title: upload
tags:
  0: API
  1: Object
  2: Properties
  4: XHR
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Returns the associated XMLHttpRequestUpload object. It can be used to gather transmission information when data is transferred to a server.'
uri: apis/xhr/XMLHttpRequest/upload

---
# upload

## Summary

Returns the associated XMLHttpRequestUpload object. It can be used to gather transmission information when data is transferred to a server.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/xhr/XMLHttpRequest](/apis/xhr/XMLHttpRequest)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = element.upload;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value"></span></span>

XMLHttpRequestUpload. Each XMLHttpRequest object has an associated XMLHttpRequestUpload object.

## Examples

``` {.js}
function transferComplete(evt) {
  alert("The transfer is complete.");
}

function transferFailed(evt) {
  alert("An error occurred while transferring the file.");
}

function transferCanceled(evt) {
  alert("The transfer has been canceled by the user.");
}

var xhr= new XMLHttpRequest();

xhr.upload.addEventListener("load", transferComplete, false);
xhr.upload.addEventListener("error", transferFailed, false);
xhr.upload.addEventListener("abort", transferCanceled, false);

xhr.open();
```

## Related specifications

Specification
:   Status
[W3C XMLHttpRequest Specification](http://www.w3.org/TR/XMLHttpRequest/)
:   W3C Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/).

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

