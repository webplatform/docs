---
title: 'status'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
notes:
  - 'Needs example. Needs a list of HTTP return codes: 200, 301, 404, 500, etc.'
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/xhr/XMLHttpRequest
    href: /apis/xhr/XMLHttpRequest
  return:
    predicate: 'Returns an object of type '
    value: 'unsigned short'
    href: /apis/xhr/XMLHttpRequest
standardization_status: 'W3C Working Draft'
summary: 'Returns the HTTP result code (status) of the response to the request.'
tags:
  - API_Object_Properties
  - API
  - XHR
  - Needs_Examples
uri: apis/xhr/XMLHttpRequest/status

---
## Summary

Returns the HTTP result code (status) of the response to the request.

Property of [apis/xhr/XMLHttpRequest](/apis/xhr/XMLHttpRequest)[apis/xhr/XMLHttpRequest](/apis/xhr/XMLHttpRequest)

## Syntax

**Note**: This property is read-only.

``` js
var result = element.status;
```

## Return Value

Returns an object of type unsigned shortunsigned short

## Related specifications

[W3C XMLHttpRequest Specification](http://www.w3.org/TR/XMLHttpRequest/)
:   W3C Working Draft
