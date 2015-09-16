---
title: 'binaryType'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/WebSockets/WebSockets_reference/WebSocket)'
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
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
summary: 'Indicates the type of binary data being transmitted by the connection.'
tags:
  0: API
  1: Object
  2: Properties
  4: WebSocket
uri: apis/websocket/WebSocket/binaryType

---
## Summary

Indicates the type of binary data being transmitted by the connection.

Property of [apis/websocket/WebSocket](/apis/websocket/WebSocket)[apis/websocket/WebSocket](/apis/websocket/WebSocket)

## Syntax

``` js
var result = element.binaryType;
element.binaryType = value;
```

## Return Value

Returns an object of type StringString

## Examples

``` js
socket.binaryType = "blob";
// receive some blob data

socket.binaryType = "arraybuffer";
// now receive ArrayBuffer data
```

## Notes

Acceptable values are "arrayBuffer" and "blob".

## Related specifications

[W3C WebSocket Specification](http://www.w3.org/TR/websockets/)
:   W3C Candidate Recommendation
