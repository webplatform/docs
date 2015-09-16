---
title: 'readyState'
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
    value: 'unsigned short'
    href: /apis/websocket/WebSocket
standardization_status: 'W3C Candidate Recommendation'
summary: 'The current state of the connection, represented as a numeric constant.'
tags:
  0: API
  1: Object
  2: Properties
  4: WebSocket
uri: apis/websocket/WebSocket/readyState

---
## Summary

The current state of the connection, represented as a numeric constant.

Property of [apis/websocket/WebSocket](/apis/websocket/WebSocket)[apis/websocket/WebSocket](/apis/websocket/WebSocket)

## Syntax

**Note**: This property is read-only.

``` js
var result = element.readyState;
```

## Return Value

Returns an object of type unsigned shortunsigned short

These constants are used by the readyState attribute to describe the state of the WebSocket connection.

|Constant|Value|Description|
|:-------|:----|:----------|
|CONNECTING|0|The connection is not yet open.|
|OPEN|1|The connection is open and ready to communicate.|
|CLOSING|2|The connection is in the process of closing.|
|CLOSED|3|The connection is closed or couldn't be opened.|

## Examples

``` js
switch (socket.readyState) {
  case WebSocket.CONNECTING:
    // do something
    break;
  case WebSocket.OPEN:
    // do something
    break;
  case WebSocket.CLOSING:
    // do something
    break;
  case WebSocket.CLOSED:
    // do something
    break;
  default:
    // this never happens
    break;
}
```

## Related specifications

[W3C WebSocket Specification](http://www.w3.org/TR/websockets/)
:   W3C Candidate Recommendation
