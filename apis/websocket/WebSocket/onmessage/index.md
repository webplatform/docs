---
title: 'onmessage'
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
summary: 'An event listener to be called when a message is received from the server. Receives a MessageEvent named &quot;message&quot;.'
tags:
  - API_Object_Properties
  - API
  - WebSocket
uri: apis/websocket/WebSocket/onmessage

---
## Summary

An event listener to be called when a message is received from the server. Receives a MessageEvent named &quot;message&quot;.

Property of [apis/websocket/WebSocket](/apis/websocket/WebSocket)[apis/websocket/WebSocket](/apis/websocket/WebSocket)

## Syntax

**Note**: This property is read-only.

``` js
var result = element.onmessage;
```

## Return Value

Returns an object of type

EventHandler

## Examples

``` js
socket.onmessage = function(event) {
  var data = event.data;
  // process data as string, blob, or ArrayBuffer
};
```

The "onmessage" event handler can also be implemented using addEventListener().

``` js
socket.addEventListener("message", function(event) {
  var data = event.data;
  // process data as string, blob, or ArrayBuffer
});
```

## Related specifications

[W3C WebSocket Specification](http://www.w3.org/TR/websockets/)
:   W3C Candidate Recommendation
