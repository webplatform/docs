---
title: readystatechange
tags:
  - Events
  - API
  - XHR
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Fires whenever the readyState of the request changes. Mostly used to determine whether the body of the response is available for handling.'
uri: apis/xhr/XMLHttpRequest/readystatechange

---
# readystatechange

## Summary

Fires whenever the readyState of the request changes. Mostly used to determine whether the body of the response is available for handling.

## Overview Table

Synchronous
:   No
Bubbles
:   No
Target
:   apis/xhr/XMLHttpRequest
Cancelable
:   No
Default action
:

## Examples

The following script demonstrates how to set an asynchronous event handler that alerts the user when the **readyState** property of the request reaches complete (`4`). Note that you must set the event handler after calling **open**, which resets all properties of the **XMLHttpRequest** object to their initial value.

``` {.js}
function reportStatus() {
    if (xhr.readyState == 4 /* complete */) {
        if (xhr.status == 200 || xhr.status == 304) {
            console.log("Transfer complete.");
        }
        else {
            // error occurred
        }
    }
}
var xhr = new XMLHttpRequest();
xhr.open("GET", "http://localhost/test.xml", true);
xhr.onreadystatechange = reportStatus;
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

