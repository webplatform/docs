---
title: reason
tags:
  0: API
  1: Object
  2: Properties
  4: WebSocket
readiness: 'Almost Ready'
standardization_status: 'W3C Candidate Recommendation'
notes:
  - 'Needs example'
summary: 'Indicates the reason the server closed the WebSocket connection.'
uri: apis/websocket/CloseEvent/reason

---
# reason

## Summary

Indicates the reason the server closed the WebSocket connection.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/websocket/CloseEvent](/apis/websocket/CloseEvent)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = element.reason;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

Reason string is specific to the particular server and sub-protocol.

**Needs Examples**: This section should include examples.

## Related specifications

Specification
:   Status
[W3C WebSocket Specification](http://www.w3.org/TR/websockets/)
:   W3C Candidate Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

