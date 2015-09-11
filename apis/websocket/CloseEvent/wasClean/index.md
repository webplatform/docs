---
title: wasClean
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
    value: Boolean
    href: /apis/websocket/CloseEvent
standardization_status: 'W3C Candidate Recommendation'
summary: 'Indicates whether the WebSocket connection was cleanly closed.'
tags:
  0: API
  1: Object
  2: Properties
  4: WebSocket
uri: apis/websocket/CloseEvent/wasClean

---
## <span>Summary</span>

Indicates whether the WebSocket connection was cleanly closed.

Property of [apis/websocket/CloseEvent](/apis/websocket/CloseEvent)[apis/websocket/CloseEvent](/apis/websocket/CloseEvent)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = element.wasClean;
```

## <span>Return Value</span>

Returns an object of type BooleanBoolean

## <span>Examples</span>

``` js


socket.onclose = function(event) {
  var wasClean = event.wasClean;
};
```

</pre>

