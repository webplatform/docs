---
title: onerror
tags:
  0: API
  1: Object
  2: Properties
  4: WebSocket
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'An event listener to be called when an error occurs. Receives an event named "error".'
uri: apis/websocket/WebSocket/onerror

---
# onerror

## Summary

An event listener to be called when an error occurs. Receives an event named "error".

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/websocket/WebSocket](/apis/websocket/WebSocket)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = element.onerror;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value"></span></span>

EventHandler

## Examples

``` {.js}
socket.onerror = function(event) {
  // handle error event
};
```

An equivalent "onerror" event handler that uses the addEventListener() method.

``` {.js}
socket.addEventListener("error", function(event) {
  // handle error event
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

