---
title: responseXML
tags:
  0: API
  1: Object
  2: Properties
  4: XHR
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
notes:
  - 'Needs example'
summary: 'Returns the response to the request as a DOM Document object, or null if the request was unsuccessful, has not yet been sent, or cannot be parsed as XML or HTML.'
uri: apis/xhr/XMLHttpRequest/responseXML

---
# responseXML

## Summary

Returns the response to the request as a DOM Document object, or null if the request was unsuccessful, has not yet been sent, or cannot be parsed as XML or HTML.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/xhr/XMLHttpRequest](/apis/xhr/XMLHttpRequest)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = element.responseXML;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value"></span></span>

DOM Document.

## Examples

``` {.js}
// The following example uses the XML DOM to display the response body

var xhr = new XMLHttpRequest();
xhr.open("GET", "http://localhost/books.xml", false);
xhr.send();
console.log(xhr.responseXML.xml);
```

## Related specifications

Specification
:   Status
[W3C XMLHttpRequest Specification](http://www.w3.org/TR/XMLHttpRequest/)
:   W3C Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

