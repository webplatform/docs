---
title: code
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/WebSockets/WebSockets_reference/CloseEvent)'
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
    value: 'unsigned short'
    href: /apis/websocket/CloseEvent
standardization_status: 'W3C Candidate Recommendation'
summary: 'The WebSocket connection close code provided by the server.'
tags:
  0: API
  1: Object
  2: Properties
  4: WebSocket
uri: apis/websocket/CloseEvent/code

---
## <span>Summary</span>

The WebSocket connection close code provided by the server.

Property of [apis/websocket/CloseEvent](/apis/websocket/CloseEvent)[apis/websocket/CloseEvent](/apis/websocket/CloseEvent)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = element.code;
```

## <span>Return Value</span>

Returns an object of type unsigned shortunsigned short

|Status code|Name|Description|
|:----------|:---|:----------|
|0-999||Reserved and not used.|
|1000|CLOSE\_NORMAL|Normal closure; the connection successfully completed whatever purpose for which it was created.|
|1001|CLOSE\_GOING\_AWAY|The endpoint is going away, either because of a server failure or because the browser is navigating away from the page that opened the connection.|
|1002|CLOSE\_PROTOCOL\_ERROR|The endpoint is terminating the connection due to a protocol error.|
|1003|CLOSE\_UNSUPPORTED|The connection is being terminated because the endpoint received data of a type it cannot accept (for example, a text-only endpoint received binary data).|
|1004|CLOSE\_TOO\_LARGE|The endpoint is terminating the connection because a data frame was received that is too large.|
|1005|CLOSE\_NO\_STATUS Reserved.|Indicates that no status code was provided even though one was expected.|
|1006|CLOSE\_ABNORMAL Reserved.|Used to indicate that a connection was closed abnormally (that is, with no close frame being sent) when a status code is expected.|
|1007-1999||Reserved for future use by the WebSocket standard.|
|2000-2999||Reserved for use by WebSocket extensions.|
|3000-3999||Available for use by libraries and frameworks. May not be used by applications.|
|4000-4999||Available for use by applications.|

**Needs Examples**: This section should include examples.

## <span>Related specifications</span>

[W3C WebSocket Specification](http://www.w3.org/TR/websockets/)
:   W3C Candidate Recommendation
