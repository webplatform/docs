---
title: 'responseXML'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
notes:
  - 'Needs example'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/xhr/XMLHttpRequest
    href: /apis/xhr/XMLHttpRequest
  return:
    predicate: 'Returns an object of type '
    value: ''
    href: /apis/xhr/XMLHttpRequest
standardization_status: 'W3C Working Draft'
summary: 'Returns the response to the request as a DOM Document object, or null if the request was unsuccessful, has not yet been sent, or cannot be parsed as XML or HTML.'
tags:
  - API_Object_Properties
  - API
  - XHR
uri: apis/xhr/XMLHttpRequest/responseXML

---
## Summary

Returns the response to the request as a DOM Document object, or null if the request was unsuccessful, has not yet been sent, or cannot be parsed as XML or HTML.

Property of [apis/xhr/XMLHttpRequest](/apis/xhr/XMLHttpRequest)[apis/xhr/XMLHttpRequest](/apis/xhr/XMLHttpRequest)

## Syntax

**Note**: This property is read-only.

``` js
var result = element.responseXML;
```

## Return Value

Returns an object of type

DOM Document.

## Examples

``` js
// The following example uses the XML DOM to display the response body

var xhr = new XMLHttpRequest();
xhr.open("GET", "http://localhost/books.xml", false);
xhr.send();
console.log(xhr.responseXML.xml);
```

## Related specifications

[W3C XMLHttpRequest Specification](http://www.w3.org/TR/XMLHttpRequest/)
:   W3C Working Draft
