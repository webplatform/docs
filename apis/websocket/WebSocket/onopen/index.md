---
title: 'onopen'
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
  - API_Object_Properties
  - API
  - WebSocket
uri: apis/websocket/WebSocket/onopen

---
## Summary

An event listener to be called when the WebSocket connection's readyState changes to OPEN. Receives an event named &quot;open&quot;.

Property of [apis/websocket/WebSocket](/apis/websocket/WebSocket)[apis/websocket/WebSocket](/apis/websocket/WebSocket)

## Syntax

**Note**: This property is read-only.

``` js
var result = element.onopen;
```

## Return Value

Returns an object of type

EventHandler

## Examples

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

## Related specifications

[W3C WebSocket Specification](http://www.w3.org/TR/websockets/)
:   W3C Candidate Recommendation
