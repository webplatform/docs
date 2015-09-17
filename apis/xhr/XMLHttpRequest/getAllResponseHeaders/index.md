---
title: 'getAllResponseHeaders'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/xhr/XMLHttpRequest
    href: /apis/xhr/XMLHttpRequest
  return_type:
    predicate: 'Returns an object of type  '
    value: String
    href: /apis/xhr/XMLHttpRequest
standardization_status: 'W3C Working Draft'
summary: 'Returns all the response headers as a string, or null if no response has been received.'
tags:
  - API_Object_Methods
  - API
  - XHR
uri: apis/xhr/XMLHttpRequest/getAllResponseHeaders

---
## Summary

Returns all the response headers as a string, or null if no response has been received.

Method of [apis/xhr/XMLHttpRequest](/apis/xhr/XMLHttpRequest)[apis/xhr/XMLHttpRequest](/apis/xhr/XMLHttpRequest)

## Syntax

``` js
var  = object.getAllResponseHeaders();
```

## Return Value

Returns an object of type StringString

## Examples

``` js
var xhr = new XMLHttpRequest();
xhr.open("GET", "http://localhost/test.xml", true);
xhr.send();

var headers = xhr.getAllResponseHeaders().toLowerCase();
alert(headers);
```

## Notes

Each name/value pair in the returned string is delimited by a carriage return/line feed (CR/LF) sequence.

## Related specifications

[W3C XMLHttpRequest Specification](http://www.w3.org/TR/XMLHttpRequest/)
:   W3C Working Draft
