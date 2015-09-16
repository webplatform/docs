---
title: MessageEvent
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/WebSockets/WebSockets_reference/MessageEvent)'
notes:
  - 'Not specific to WebSocket. Probably belongs somewhere in the DOM docs.'
readiness: 'In Progress'
summary: 'A MessageEvent is sent to clients using WebSockets when data is received from the server. This is delivered to the listener indicated by the WebSocket object''s onmessage attribute.'
tags:
  - API
  - Objects
uri: apis/websocket/MessageEvent

---
## Summary

A MessageEvent is sent to clients using WebSockets when data is received from the server. This is delivered to the listener indicated by the WebSocket object's onmessage attribute.

## Properties

API Name
:   Summary

[html/elements/data](/apis/websocket/MessageEvent/data)
:   The data from the server.

## Methods

*No methods.*

## Events

*No events.*

## Examples

``` js


socket.onmessage = function (event) {
  console.log(event.data);
}
```

</pre>

