---
title: setRequestHeader
tags:
  0: API
  1: Object
  2: Methods
  4: XHR
readiness: 'Almost Ready'
standardization_status: 'W3C Working Draft'
notes:
  - 'Needs example'
summary: 'Sets the value of an XMLHttpRequest header.'
uri: apis/xhr/XMLHttpRequest/setRequestHeader

---
# setRequestHeader

## Summary

Sets the value of an XMLHttpRequest header.

*Method of [apis/xhr/XMLHttpRequest](/apis/xhr/XMLHttpRequest)*

## Syntax

``` {.js}
 object.setRequestHeader(header, value);
```

## Parameters

### header

 Data-typeÂ
:   String

 Specifies the header name.

### value

 Data-typeÂ
:   String

 Specifies the header value.

## Return Value

No return value

**Needs Examples**: This section should include examples.

## Usage

     If used, must be called after open(), but before send().

## Notes

Refer to [RFC2616, Section 14: Header Field Definitions](http://go.microsoft.com/fwlink/p/?linkid=203727) for a general list of standard headers. The server is ultimately responsible for honoring the headers of the request. By far the most common request header is Content-Type, which is required by some XML Web services.

## Related specifications

Specification
:   Status
[W3C XMLHttpRequest Specification](http://www.w3.org/TR/XMLHttpRequest/)
:   W3C Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

