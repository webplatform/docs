---
title: withCredentials
tags:
  0: API
  1: Object
  2: Properties
  4: XHR
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Returns or sets whether cross-site Access-Control requests should be made using credentials such as cookies or authorization headers.'
uri: apis/xhr/XMLHttpRequest/withCredentials

---
# withCredentials

## Summary

Returns or sets whether cross-site Access-Control requests should be made using credentials such as cookies or authorization headers.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/xhr/XMLHttpRequest](/apis/xhr/XMLHttpRequest)</span></span>

## Syntax

``` {.js}
var result = element.withCredentials;
element.withCredentials = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Boolean</span></span>

Default is *false*.

## Examples

``` {.js}
var xhr = new XMLHttpRequest();
xhr.open("GET", "http://updates.html5rocks.com", true);
xhr.withCredentials = true;
xhr.send();
```

## Notes

withCredentials cannot be set after the XMLHttpRequest's [**send()**](/apis/xhr/XMLHttpRequest/send) method is called.

## Related specifications

Specification
:   Status
[W3C XMLHttpRequest Specification](http://www.w3.org/TR/XMLHttpRequest/)
:   W3C Working Draft
[Cross-Origin Resource Sharing](http://www.w3.org/TR/cors/)
:   W3C Candidate Recommendation 29 January 2013

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

