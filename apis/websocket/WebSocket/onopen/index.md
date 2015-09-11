---
title: onopen
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/websocket/WebSocket
    href: /apis/websocket/WebSocket
  return:
    predicate: 'Returns an object of type '
    value: ''
    href: /apis/websocket/WebSocket
standardization_status: 'W3C Candidate Recommendation'
summary: 'An event listener to be called when the WebSocket connection''s readyState changes to OPEN. Receives an event named &quot;open&quot;.'
tags:
  0: API
  1: Object
  2: Properties
  4: WebSocket
uri: apis/websocket/WebSocket/onopen

---
## <span>Summary</span>

An event listener to be called when the WebSocket connection's readyState changes to OPEN. Receives an event named &quot;open&quot;.

Property of [apis/websocket/WebSocket](/apis/websocket/WebSocket)[apis/websocket/WebSocket](/apis/websocket/WebSocket)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = element.onopen;
```

## <span>Return Value</span>

Returns an object of type<span></span>

EventHandler

## <span>Examples</span>

``` js
socket.onopen = function(event) {
  // handle open event
};
```

Event handlers can also be created using the addEventListener() method.

``` js
socket.addEventListener("open", function(event) {
  // handle open event
});
```

## <span>Related specifications</span>

[W3C WebSocket Specification](http://www.w3.org/TR/websockets/)
:   W3C Candidate Recommendation
