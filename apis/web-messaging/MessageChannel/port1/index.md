---
title: port1
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/web-messaging/MessageChannel
    href: /apis/web-messaging/MessageChannel
  return:
    predicate: 'Returns an object of type '
    value: ''
    href: /apis/web-messaging/MessageChannel
standardization_status: 'W3C Candidate Recommendation'
summary: 'Returns the first MessagePort object of the MessageChannel.'
tags:
  0: API
  1: Object
  2: Properties
  4: Web
  5: Messaging
uri: apis/web-messaging/MessageChannel/port1

---
## Summary

Returns the first MessagePort object of the MessageChannel.

Property of [apis/web-messaging/MessageChannel](/apis/web-messaging/MessageChannel)[apis/web-messaging/MessageChannel](/apis/web-messaging/MessageChannel)

## Syntax

**Note**: This property is read-only.

``` js
var result = element.port1;
```

## Return Value

Returns an object of type

MessagePort

## Examples

This example creates a new message channel and uses one of the ports to send a message, which will be received by the other port.

``` js
var msgChannel = new MessageChannel();
msgChannel.port1.postMessage('Hello world');
```

## Notes

Communication channels in this mechanism are implemented as two-way pipes, with a port at each end. Messages sent in one port are delivered at the other port, and vice versa. Messages are asynchronous, and delivered as DOM events.

## Related specifications

[W3C Web Messaging Specification](http://www.w3.org/TR/webmessaging/)
:   W3C Candidate Recommendation
