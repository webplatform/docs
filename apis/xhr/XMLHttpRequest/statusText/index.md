---
title: statusText
tags:
  0: API
  1: Object
  2: Properties
  4: XHR
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
notes:
  - 'Needs example'
summary: 'Returns the HTTP status text.'
uri: apis/xhr/XMLHttpRequest/statusText

---
# statusText

## Summary

Returns the HTTP status text.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/xhr/XMLHttpRequest](/apis/xhr/XMLHttpRequest)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = element.statusText;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

## Examples

``` {.js}
// The following script checks the status to determine if the request was successful
var xhr = new XMLHttpRequest();
xhr.open("GET", "http://localhost/test.xml", false);
xhr.send()
if (xhr.statusText == "OK")
   console.log(xhr.responseText);
else
   console.log(xhr.statusText);
```

## Related specifications

Specification
:   Status
[W3C XMLHttpRequest Specification](http://www.w3.org/TR/XMLHttpRequest/)
:   W3C Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

