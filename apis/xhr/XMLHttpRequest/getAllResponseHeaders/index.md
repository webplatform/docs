---
title: getAllResponseHeaders
tags:
  0: API
  1: Object
  2: Methods
  4: XHR
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Returns all the response headers as a string, or null if no response has been received.'
uri: apis/xhr/XMLHttpRequest/getAllResponseHeaders

---
# getAllResponseHeaders

## Summary

Returns all the response headers as a string, or null if no response has been received.

*Method of [apis/xhr/XMLHttpRequest](/apis/xhr/XMLHttpRequest)*

## Syntax

``` {.js}
var  = object.getAllResponseHeaders();
```

## Return Value

Returns an object of type String.

## Examples

``` {.js}
var xhr = new XMLHttpRequest();
xhr.open("GET", "http://localhost/test.xml", true);
xhr.send();

var headers = xhr.getAllResponseHeaders().toLowerCase();
alert(headers);
```

## Notes

Each name/value pair in the returned string is delimited by a carriage return/line feed (CR/LF) sequence.

## Related specifications

Specification
:   Status
[W3C XMLHttpRequest Specification](http://www.w3.org/TR/XMLHttpRequest/)
:   W3C Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

