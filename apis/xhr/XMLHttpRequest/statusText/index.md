---
title: statusText
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
    value: String
    href: /apis/xhr/XMLHttpRequest
standardization_status: 'W3C Working Draft'
summary: 'Returns the HTTP status text.'
tags:
  0: API
  1: Object
  2: Properties
  4: XHR
uri: apis/xhr/XMLHttpRequest/statusText

---
## Summary

Returns the HTTP status text.

Property of [apis/xhr/XMLHttpRequest](/apis/xhr/XMLHttpRequest)[apis/xhr/XMLHttpRequest](/apis/xhr/XMLHttpRequest)

## Syntax

**Note**: This property is read-only.

``` js
var result = element.statusText;
```

## Return Value

Returns an object of type StringString

## Examples

``` js
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

[W3C XMLHttpRequest Specification](http://www.w3.org/TR/XMLHttpRequest/)
:   W3C Working Draft
