---
title: code
tags:
  0: API
  1: Object
  2: Properties
  4: WebSocket
readiness: 'Almost Ready'
standardization_status: 'W3C Candidate Recommendation'
notes:
  - 'Needs example'
summary: 'The WebSocket connection close code provided by the server.'
uri: apis/websocket/CloseEvent/code

---
# code

## Summary

The WebSocket connection close code provided by the server.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/websocket/CloseEvent](/apis/websocket/CloseEvent)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = element.code;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">unsigned short</span></span>

Status code
:   Name
0-999
:
1000
:   CLOSE\_NORMAL
1001
:   CLOSE\_GOING\_AWAY
1002
:   CLOSE\_PROTOCOL\_ERROR
1003
:   CLOSE\_UNSUPPORTED
1004
:   CLOSE\_TOO\_LARGE
1005
:   CLOSE\_NO\_STATUS Reserved.
1006
:   CLOSE\_ABNORMAL Reserved.
1007-1999
:
2000-2999
:
3000-3999
:
4000-4999
:

**Needs Examples**: This section should include examples.

## Related specifications

Specification
:   Status
[W3C WebSocket Specification](http://www.w3.org/TR/websockets/)
:   W3C Candidate Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/WebSockets/WebSockets_reference/CloseEvent)

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

