---
title: onclose
tags:
  0: API
  1: Object
  2: Properties
  4: WebSocket
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'An event listener to be called when the WebSocket connection''s readyState changes to CLOSED. Receives a CloseEvent named "close".'
uri: apis/websocket/WebSocket/onclose

---
# onclose

## Summary

An event listener to be called when the WebSocket connection's readyState changes to CLOSED. Receives a CloseEvent named "close".

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/websocket/WebSocket](/apis/websocket/WebSocket)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = element.onclose;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value"></span></span>

EventHandler

## Examples

``` {.js}
socket.onclose = function(event) {
  var code = event.code;
  var reason = event.reason;
  var wasClean = event.wasClean;
  // handle close event
};
```

## Related specifications

Specification
:   Status
[W3C WebSocket Specification](http://www.w3.org/TR/websockets/)
:   W3C Candidate Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

