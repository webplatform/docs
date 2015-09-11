---
title: timeout
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
    value: 'unsigned long'
    href: /apis/xhr/XMLHttpRequest
standardization_status: 'W3C Working Draft'
summary: 'Returns or sets the number of milliseconds a request can take before automatically being terminated.'
tags:
  0: API
  1: Object
  2: Properties
  4: XHR
uri: apis/xhr/XMLHttpRequest/timeout

---
## <span>Summary</span>

Returns or sets the number of milliseconds a request can take before automatically being terminated.

Property of [apis/xhr/XMLHttpRequest](/apis/xhr/XMLHttpRequest)[apis/xhr/XMLHttpRequest](/apis/xhr/XMLHttpRequest)

## <span>Syntax</span>

``` js
var result = element.timeout;
element.timeout = value;
```

## <span>Return Value</span>

Returns an object of type unsigned longunsigned long

## <span>Examples</span>

``` js
// The following example sets the timeout property

var xhr = new XMLHttpRequest();
xhr.open("GET", "http://localhost/books.xml", true);
xhr.timeout = 10000;
xhr.ontimeout = timeoutFired;
xhr.send(null);
```

## <span>Notes</span>

The **timeout** property has a default value of 0. If the time-out period expires, the **responseText** property will be null. You should set a time-out value that is slightly longer than the expected response time of the request. The **timeout** property may be set only in the time interval between a call to the **open** method and the first call to the **send** method. If you set an **XMLHttpRequest** time-out value that is larger than the network stack's time-out value, the network stack will time out first and the **ontimeout** event will not be raised.

## <span>Related specifications</span>

[W3C XMLHttpRequest Specification](http://www.w3.org/TR/XMLHttpRequest/)
:   W3C Working Draft
