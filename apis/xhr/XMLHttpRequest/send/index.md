---
title: send
tags:
  0: API
  1: Object
  2: Methods
  4: XHR
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
notes:
  - 'Needs example'
summary: 'Initiates the request defined by the XMLHttpRequest.'
uri: apis/xhr/XMLHttpRequest/send

---
# send

## Summary

Initiates the request defined by the XMLHttpRequest.

*Method of [apis/xhr/XMLHttpRequest](/apis/xhr/XMLHttpRequest)*

## Syntax

``` {.js}
 .send(data);
```

## Parameters

### data

 Data-typeÂ
:   any

*(Optional)*

Object that specifies the body of the message being sent with the request. May be any one of **ArrayBuffer**, **Blob**, **Document**, **DOMString**, or **FormData** object types.

## Return Value

No return value

## Examples

``` {.js}
var xhr = new XMLHttpRequest();
xhr.open("GET", "http://localhost/test.xml", true);
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

