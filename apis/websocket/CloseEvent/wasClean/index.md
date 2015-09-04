---
title: wasClean
tags:
  0: API
  1: Object
  2: Properties
  4: WebSocket
readiness: 'Almost Ready'
standardization_status: 'W3C Candidate Recommendation'
notes:
  - 'Needs example'
summary: 'Indicates whether the WebSocket connection was cleanly closed.'
uri: apis/websocket/CloseEvent/wasClean

---
# wasClean

## Summary

Indicates whether the WebSocket connection was cleanly closed.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/websocket/CloseEvent](/apis/websocket/CloseEvent)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = element.wasClean;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Boolean</span></span>

## Examples

``` {.js}


socket.onclose = function(event) {
  var wasClean = event.wasClean;
};
```

</pre>

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/WebSockets/WebSockets_reference/CloseEvent)

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

