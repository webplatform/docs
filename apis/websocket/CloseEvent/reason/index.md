---
title: reason
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
notes:
  - 'Needs example'
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/websocket/CloseEvent
    href: /apis/websocket/CloseEvent
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /apis/websocket/CloseEvent
standardization_status: 'W3C Candidate Recommendation'
summary: 'Indicates the reason the server closed the WebSocket connection.'
tags:
  0: API
  1: Object
  2: Properties
  4: WebSocket
uri: apis/websocket/CloseEvent/reason

---
## Summary

Indicates the reason the server closed the WebSocket connection.

Property of [apis/websocket/CloseEvent](/apis/websocket/CloseEvent)[apis/websocket/CloseEvent](/apis/websocket/CloseEvent)

## Syntax

**Note**: This property is read-only.

``` js
var result = element.reason;
```

## Return Value

Returns an object of type StringString

Reason string is specific to the particular server and sub-protocol.

**Needs Examples**: This section should include examples.

## Related specifications

[W3C WebSocket Specification](http://www.w3.org/TR/websockets/)
:   W3C Candidate Recommendation
