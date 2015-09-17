---
title: 'getResponseHeader'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
notes:
  - 'Needs example, spec reference, standardization status'
readiness: 'In Progress'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/xhr/XMLHttpRequest
    href: /apis/xhr/XMLHttpRequest
  return_type:
    predicate: 'Returns an object of type  '
    value: ''
    href: /apis/xhr/XMLHttpRequest
summary: 'Returns the string containing the text of the specified header, or null if the response has not been received or the header does not exist.'
tags:
  - API_Object_Methods
  - API
  - XHR
  - Needs_Examples
uri: apis/xhr/XMLHttpRequest/getResponseHeader

---
## Summary

Returns the string containing the text of the specified header, or null if the response has not been received or the header does not exist.

Method of [apis/xhr/XMLHttpRequest](/apis/xhr/XMLHttpRequest)[apis/xhr/XMLHttpRequest](/apis/xhr/XMLHttpRequest)

## Syntax

``` js
var  = object.getResponseHeader(header);
```

## Parameters

### header

 Data-type
:   String

 String that specifies the response header name.

## Return Value

Returns an object of type

ByteString
