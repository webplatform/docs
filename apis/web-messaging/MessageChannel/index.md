---
title: 'MessageChannel'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Creates a connection (two &quot;entangled&quot; ports) to enable independent pieces of code (running in different browsing contexts) to communicate directly.'
tags:
  0: API
  1: Objects
  3: Web
  4: Messaging
uri: apis/web-messaging/MessageChannel

---
## Summary

Creates a connection (two &quot;entangled&quot; ports) to enable independent pieces of code (running in different browsing contexts) to communicate directly.

## Properties

API Name
:   Summary

[port1](/apis/web-messaging/MessageChannel/port1)
:   Returns the first MessagePort object of the MessageChannel.

[port2](/apis/web-messaging/MessageChannel/port2)
:   Returns the second MessagePort object.

## Methods

*No methods.*

## Events

*No events.*

## Examples

``` js
var msgChannel = new MessageChannel();
```

## Notes

When you create a new **MessageChannel** object, it has two connected **MessagePort** objects (**port1** and **port2**). One of the ports is sent to another window or frame, and messages can be sent and received without the repeated origin checking that is needed when using **window.postMessage**. Validation of the origin of a port and messages need only be done when a port is sent to windows other than the one that created them. **MessagePort** simplifies the messaging process by sending and receiving messages through two (and only those two) connected ports.

Messages are posted between the ports using **postMessage**. As the ports will only accept messages between the connected ports, no further validation is required once the connection is established. **MessageChannel** enables asynchronous communication between **IFrameElements**, cross-domain windows, or same page communications.

## Related specifications

[W3C Web Messaging Specification](http://www.w3.org/TR/webmessaging/)
:   W3C Candidate Recommendation
