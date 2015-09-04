---
title: port1
tags:
  0: API
  1: Object
  2: Properties
  4: Web
  5: Messaging
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Returns the first MessagePort object of the MessageChannel.'
uri: apis/web-messaging/MessageChannel/port1

---
# port1

## Summary

Returns the first MessagePort object of the MessageChannel.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/web-messaging/MessageChannel](/apis/web-messaging/MessageChannel)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = element.port1;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value"></span></span>

MessagePort

## Examples

This example creates a new message channel and uses one of the ports to send a message, which will be received by the other port.

``` {.js}
var msgChannel = new MessageChannel();
msgChannel.port1.postMessage('Hello world');
```

## Notes

Communication channels in this mechanism are implemented as two-way pipes, with a port at each end. Messages sent in one port are delivered at the other port, and vice versa. Messages are asynchronous, and delivered as DOM events.

## Related specifications

Specification
:   Status
[W3C Web Messaging Specification](http://www.w3.org/TR/webmessaging/)
:   W3C Candidate Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

