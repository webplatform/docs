---
title: 'MessagePort'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Exposes the available methods on the connected ports.'
tags:
  0: API
  1: Objects
  3: Web
  4: Messaging
uri: apis/web-messaging/MessagePort

---
## Summary

Exposes the available methods on the connected ports.

## Properties

*No properties.*

## Methods

API Name
:   Summary

[close](/apis/web-messaging/MessagePort/close)
:   Disconnects the port, so that it is no longer active.

[postMessage](/apis/web-messaging/MessagePort/postMessage)
:   Posts a message through the channel, from one port to the other.

[start](/apis/web-messaging/MessagePort/start)
:   Begins dispatching messages received on the port. See Notes.

## Events

*No events.*

## Notes

Two **MessagePort** objects are automatically created when a **MessageChannel** object is created, and are returned by the **port1** and **port2** properties. Messages are sent from one port are received by the other, and vice versa. The **MessagePort** object provides the **start** method to begin dispatching messages received on the port, and the **close** method to close and disconnect the port. The **postMessage** method sends messages through the port. In Internet Explorer 10, message ports are automatically enabled when a message event is registered with the **onmessage** property or **addEventListener** method. This makes it unnecessary to explicitly call the **start** method under these conditions. After posting a **MessagePort** object using **postMessage**, the **MessagePort** object is implicitly **close**d.

## Related specifications

[W3C Web Messaging Specification](http://www.w3.org/TR/webmessaging/)
:   W3C Candidate Recommendation
