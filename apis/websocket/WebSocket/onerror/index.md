---
title: 'onerror'
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
summary: 'An event listener to be called when an error occurs. Receives an event named &quot;error&quot;.'
tags:
  0: API
  1: Object
  2: Properties
  4: WebSocket
uri: apis/websocket/WebSocket/onerror

---
## Summary

An event listener to be called when an error occurs. Receives an event named &quot;error&quot;.

Property of [apis/websocket/WebSocket](/apis/websocket/WebSocket)[apis/websocket/WebSocket](/apis/websocket/WebSocket)

## Syntax

**Note**: This property is read-only.

``` js
var result = element.onerror;
```

## Return Value

Returns an object of type

EventHandler

## Examples

``` js
socket.onerror = function(event) {
  // handle error event
};
```

An equivalent "onerror" event handler that uses the addEventListener() method.

``` js
socket.addEventListener("error", function(event) {
  // handle error event
});
```

## Related specifications

[W3C WebSocket Specification](http://www.w3.org/TR/websockets/)
:   W3C Candidate Recommendation
