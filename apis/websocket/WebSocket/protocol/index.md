---
title: protocol
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/WebSockets/WebSockets_reference/WebSocket)'
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
notes:
  - 'Needs example'
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/websocket/WebSocket
    href: /apis/websocket/WebSocket
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /apis/websocket/WebSocket
standardization_status: 'W3C Candidate Recommendation'
summary: 'Indicates the name of the sub-protocol the server selected.'
tags:
  0: API
  1: Object
  2: Properties
  4: WebSocket
uri: apis/websocket/WebSocket/protocol

---
## <span>Summary</span>

Indicates the name of the sub-protocol the server selected.

Property of [apis/websocket/WebSocket](/apis/websocket/WebSocket)[apis/websocket/WebSocket](/apis/websocket/WebSocket)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = element.protocol;
```

## <span>Return Value</span>

Returns an object of type StringString

This will be one of the strings specified in the *protocol* parameter when creating the **WebSocket** object.

**Needs Examples**: This section should include examples.

## <span>Notes</span>

Protocol negotiation is part of the **WebSocket** connection handshake. The protocol value is not set until the connection is established. If the client specifies one or more protocols, the server returns one or none of the protocols during the protocol negotiation in the handshake. After the connection is established, then the protocol value is either empty or set to the protocol that was accepted.

## <span>Related specifications</span>

[W3C WebSocket Specification](http://www.w3.org/TR/websockets/)
:   W3C Candidate Recommendation
