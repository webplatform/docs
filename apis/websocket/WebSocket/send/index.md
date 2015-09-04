---
title: send
tags:
  0: API
  1: Object
  2: Methods
  4: WebSocket
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Transmits data to the server over the WebSocket connection.'
uri: apis/websocket/WebSocket/send

---
# send

## Summary

Transmits data to the server over the WebSocket connection.

*Method of [apis/websocket/WebSocket](/apis/websocket/WebSocket)*

## Syntax

``` {.js}
 object.send(data);
```

## Parameters

### data

 Data-typeÂ
:   any

 Must be of one of the following types:

-   String
-   Blob
-   ArrayBuffer
-   ArrayBufferView

## Return Value

No return value

## Examples

``` {.js}
var data = new ArrayBuffer(10000000);

// perform some operations on the ArrayBuffer
socket.send(data);

if (socket.bufferedAmount === 0) {
  // the data sent
}
else {
  // the data did not send
}
```

## Notes

An **ArrayBuffer** is a unformatted block of raw data that is sent in its entirety to a server. An ArrayBufferView is a typed array view of an **ArrayBuffer**. By using a typed array to define the format of the buffer, and the start and length (number of elements), you can send portions of an **ArrayBuffer** to a server. This method can throw one of the following exceptions:

Exception
:   Description
InvalidStateError(11)
:   The connection is not currently OPEN.

## Related specifications

Specification
:   Status
[W3C WebSocket Specification](http://www.w3.org/TR/websockets/)
:   W3C Candidate Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/WebSockets/WebSockets_reference/WebSocket)

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

