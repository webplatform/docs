---
title: 'setRequestHeader'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
notes:
  - 'Needs example'
readiness: 'Almost Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/xhr/XMLHttpRequest
    href: /apis/xhr/XMLHttpRequest
standardization_status: 'W3C Working Draft'
summary: 'Sets the value of an XMLHttpRequest header.'
tags:
  - API_Object_Methods
  - API
  - XHR
  - Needs_Examples
uri: apis/xhr/XMLHttpRequest/setRequestHeader

---
## Summary

Sets the value of an XMLHttpRequest header.

Method of [apis/xhr/XMLHttpRequest](/apis/xhr/XMLHttpRequest)[apis/xhr/XMLHttpRequest](/apis/xhr/XMLHttpRequest)

## Syntax

``` js
 object.setRequestHeader(header, value);
```

## Parameters

### header

 Data-type
:   String

 Specifies the header name.

### value

 Data-type
:   String

 Specifies the header value.

## Return Value

No return value

## Usage

     If used, must be called after open(), but before send().

## Notes

Refer to [RFC2616, Section 14: Header Field Definitions](http://go.microsoft.com/fwlink/p/?linkid=203727) for a general list of standard headers. The server is ultimately responsible for honoring the headers of the request. By far the most common request header is Content-Type, which is required by some XML Web services.

## Related specifications

[W3C XMLHttpRequest Specification](http://www.w3.org/TR/XMLHttpRequest/)
:   W3C Working Draft
