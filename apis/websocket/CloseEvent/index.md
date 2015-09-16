---
title: 'CloseEvent'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Object representing the close event for a WebSocket.'
tags:
  0: API
  1: Objects
  3: WebSocket
uri: apis/websocket/CloseEvent

---
## Summary

Object representing the close event for a WebSocket.

## Properties

API Name
:   Summary

[code](/apis/websocket/CloseEvent/code)
:   The WebSocket connection close code provided by the server.

[reason](/apis/websocket/CloseEvent/reason)
:   Indicates the reason the server closed the WebSocket connection.

[wasClean](/apis/websocket/CloseEvent/wasClean)
:   Indicates whether the WebSocket connection was cleanly closed.

## Methods

*No methods.*

## Events

*No events.*

## Examples

``` js


socket.onclose = function(event) {
  var code = event.code;
  var reason = event.reason;
  var wasClean = event.wasClean;
  // handle close event
};
```

</pre>

## Notes

When a WebSocket connection is closed, possibly cleanly, the user agent must create an [event](/apis/websocket/WebSocket/onclose) that uses the CloseEvent interface, with the event name close, which does not bubble, is not cancelable, has no default action, whose [wasClean](/apis/websocket/CloseEvent/wasClean) attribute is set to true if the connection closed cleanly and false otherwise, whose code attribute is set to the WebSocket connection close code, and whose [reason](/apis/websocket/CloseEvent/reason) attribute is set to the WebSocket connection close reason; and then queue a task to first change the [readyState](/apis/websocket/WebSocket/readyState) attribute's value to CLOSED (3), and then [dispatch the event](/apis/websocket/WebSocket/onclose) at the [WebSocket object](/apis/websocket/WebSocket).

## Related specifications

[W3C WebSocket Specification](http://www.w3.org/TR/websockets/)
:   W3C Candidate Recommendation
