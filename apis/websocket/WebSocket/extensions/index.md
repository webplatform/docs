---
title: 'extensions'
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
summary: 'The extensions selected by the server.'
tags:
  0: API
  1: Object
  2: Properties
  4: WebSocket
uri: apis/websocket/WebSocket/extensions

---
## Summary

The extensions selected by the server.

Property of [apis/websocket/WebSocket](/apis/websocket/WebSocket)[apis/websocket/WebSocket](/apis/websocket/WebSocket)

## Syntax

**Note**: This property is read-only.

``` js
var result = element.extensions;
```

## Return Value

Returns an object of type StringString

**Needs Examples**: This section should include examples.

## Notes

This is either the empty string or a list of extensions as negotiated by the connection.

Currently, Windows Internet Explorer does not support any extensions. The property always returns an empty string.

## Related specifications

[W3C WebSocket Specification](http://www.w3.org/TR/websockets/)
:   W3C Candidate Recommendation
