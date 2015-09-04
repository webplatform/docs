---
title: onmessage
tags:
  0: API
  1: Object
  2: Properties
  4: WebSocket
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'An event listener to be called when a message is received from the server. Receives a MessageEvent named "message".'
uri: apis/websocket/WebSocket/onmessage

---
# onmessage

## Summary

An event listener to be called when a message is received from the server. Receives a MessageEvent named "message".

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/websocket/WebSocket](/apis/websocket/WebSocket)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = element.onmessage;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value"></span></span>

EventHandler

## Examples

``` {.js}
socket.onmessage = function(event) {
  var data = event.data;
  // process data as string, blob, or ArrayBuffer
};
```

The "onmessage" event handler can also be implemented using addEventListener().

``` {.js}
socket.addEventListener("message", function(event) {
  var data = event.data;
  // process data as string, blob, or ArrayBuffer
});
```

## Related specifications

Specification
:   Status
[W3C WebSocket Specification](http://www.w3.org/TR/websockets/)
:   W3C Candidate Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

