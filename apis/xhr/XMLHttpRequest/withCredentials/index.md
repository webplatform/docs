---
title: withCredentials
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/xhr/XMLHttpRequest
    href: /apis/xhr/XMLHttpRequest
  return:
    predicate: 'Returns an object of type '
    value: Boolean
    href: /apis/xhr/XMLHttpRequest
standardization_status: 'W3C Working Draft'
summary: 'Returns or sets whether cross-site Access-Control requests should be made using credentials such as cookies or authorization headers.'
tags:
  0: API
  1: Object
  2: Properties
  4: XHR
uri: apis/xhr/XMLHttpRequest/withCredentials

---
## <span>Summary</span>

Returns or sets whether cross-site Access-Control requests should be made using credentials such as cookies or authorization headers.

Property of [apis/xhr/XMLHttpRequest](/apis/xhr/XMLHttpRequest)[apis/xhr/XMLHttpRequest](/apis/xhr/XMLHttpRequest)

## <span>Syntax</span>

``` js
var result = element.withCredentials;
element.withCredentials = value;
```

## <span>Return Value</span>

Returns an object of type BooleanBoolean

Default is *false*.

## <span>Examples</span>

``` js
var xhr = new XMLHttpRequest();
xhr.open("GET", "http://updates.html5rocks.com", true);
xhr.withCredentials = true;
xhr.send();
```

## <span>Notes</span>

withCredentials cannot be set after the XMLHttpRequest's [**send()**](/apis/xhr/XMLHttpRequest/send) method is called.

## <span>Related specifications</span>

[W3C XMLHttpRequest Specification](http://www.w3.org/TR/XMLHttpRequest/)
:   W3C Working Draft

[Cross-Origin Resource Sharing](http://www.w3.org/TR/cors/)
:   W3C Candidate Recommendation 29 January 2013
