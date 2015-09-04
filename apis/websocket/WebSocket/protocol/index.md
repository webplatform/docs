---
title: protocol
tags:
  0: API
  1: Object
  2: Properties
  4: WebSocket
readiness: 'Almost Ready'
standardization_status: 'W3C Candidate Recommendation'
notes:
  - 'Needs example'
summary: 'Indicates the name of the sub-protocol the server selected.'
uri: apis/websocket/WebSocket/protocol

---
# protocol

## Summary

Indicates the name of the sub-protocol the server selected.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/websocket/WebSocket](/apis/websocket/WebSocket)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = element.protocol;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

This will be one of the strings specified in the *protocol* parameter when creating the **WebSocket** object.

**Needs Examples**: This section should include examples.

## Notes

Protocol negotiation is part of the **WebSocket** connection handshake. The protocol value is not set until the connection is established. If the client specifies one or more protocols, the server returns one or none of the protocols during the protocol negotiation in the handshake. After the connection is established, then the protocol value is either empty or set to the protocol that was accepted.

## Related specifications

Specification
:   Status
[W3C WebSocket Specification](http://www.w3.org/TR/websockets/)
:   W3C Candidate Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/WebSockets/WebSockets_reference/WebSocket)

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

