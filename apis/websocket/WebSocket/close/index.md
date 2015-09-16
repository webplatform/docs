---
title: close
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/WebSockets/WebSockets_reference/WebSocket)'
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
notes:
  - 'Needs example'
readiness: 'Almost Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/websocket/WebSocket
    href: /apis/websocket/WebSocket
standardization_status: 'W3C Candidate Recommendation'
summary: 'Closes the WebSocket connection or connection attempt, if any.'
tags:
  0: API
  1: Object
  2: Methods
  4: WebSocket
uri: apis/websocket/WebSocket/close

---
## Summary

Closes the WebSocket connection or connection attempt, if any.

Method of [apis/websocket/WebSocket](/apis/websocket/WebSocket)[apis/websocket/WebSocket](/apis/websocket/WebSocket)

## Syntax

``` js
 object.close(code, reason);
```

## Parameters

### code

 Data-type
:   unsigned short

(Optional)

A numeric value indicating the status code explaining why the connection is being closed. If this parameter is not specified, a default value of 1000 (indicating a normal "transaction complete" closure) is assumed.

### reason

 Data-type
:   String

(Optional)

A human-readable string explaining why the connection is closing. This string must be no longer than 123 bytes of UTF-8 text (not characters).

## Return Value

No return value

**Needs Examples**: This section should include examples.

## Notes

The **onclose** event will return three attributes:

-   **wasClean** (binary) - whether the connection closed cleanly.
-   **code** (unsigned long) - code from the server.
-   **reason** (text) - reason provided by the server.

If the *code* parameter is present but is not an integer equal to 1000 or in the range 3000 to 4999, this method throws an **InvalidAccessError** exception and aborts. If the *reason* parameter is longer than 123 bytes this method throws a **SyntaxError** exception, and aborts.

## Related specifications

[W3C WebSocket Specification](http://www.w3.org/TR/websockets/)
:   W3C Candidate Recommendation
