---
title: 'onclose'
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
summary: 'An event listener to be called when the WebSocket connection''s readyState changes to CLOSED. Receives a CloseEvent named &quot;close&quot;.'
tags:
  - API_Object_Properties
  - API
  - WebSocket
uri: apis/websocket/WebSocket/onclose

---
## Summary

An event listener to be called when the WebSocket connection's readyState changes to CLOSED. Receives a CloseEvent named &quot;close&quot;.

Property of [apis/websocket/WebSocket](/apis/websocket/WebSocket)[apis/websocket/WebSocket](/apis/websocket/WebSocket)

## Syntax

**Note**: This property is read-only.

``` js
var result = element.onclose;
```

## Return Value

Returns an object of type

EventHandler

## Examples

``` js
socket.onclose = function(event) {
  var code = event.code;
  var reason = event.reason;
  var wasClean = event.wasClean;
  // handle close event
};
```

## Related specifications

[W3C WebSocket Specification](http://www.w3.org/TR/websockets/)
:   W3C Candidate Recommendation
