---
title: setRequestHeader
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
  0: API
  1: Object
  2: Methods
  4: XHR
uri: apis/xhr/XMLHttpRequest/setRequestHeader

---
## <span>Summary</span>

Sets the value of an XMLHttpRequest header.

Method of [apis/xhr/XMLHttpRequest](/apis/xhr/XMLHttpRequest)[apis/xhr/XMLHttpRequest](/apis/xhr/XMLHttpRequest)

## <span>Syntax</span>

``` js
 object.setRequestHeader(header, value);
```

## <span>Parameters</span>

### <span>header</span>

 Data-type
:   String

 Specifies the header name.

### <span>value</span>

 Data-type
:   String

 Specifies the header value.

## <span>Return Value</span>

No return value

**Needs Examples**: This section should include examples.

## <span>Usage</span>

     If used, must be called after open(), but before send().

## <span>Notes</span>

Refer to [RFC2616, Section 14: Header Field Definitions](http://go.microsoft.com/fwlink/p/?linkid=203727) for a general list of standard headers. The server is ultimately responsible for honoring the headers of the request. By far the most common request header is Content-Type, which is required by some XML Web services.

## <span>Related specifications</span>

[W3C XMLHttpRequest Specification](http://www.w3.org/TR/XMLHttpRequest/)
:   W3C Working Draft
