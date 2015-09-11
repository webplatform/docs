---
title: start
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/web-messaging/MessagePort
    href: /apis/web-messaging/MessagePort
standardization_status: 'W3C Candidate Recommendation'
summary: 'Begins dispatching messages received on the port. See Notes.'
tags:
  0: API
  1: Object
  2: Methods
  4: Web
  5: Messaging
uri: apis/web-messaging/MessagePort/start

---
## <span>Summary</span>

Begins dispatching messages received on the port. See Notes.

Method of [apis/web-messaging/MessagePort](/apis/web-messaging/MessagePort)[apis/web-messaging/MessagePort](/apis/web-messaging/MessagePort)

## <span>Syntax</span>

``` js
 MessagePort.start();
```

## <span>Return Value</span>

No return value

## <span>Examples</span>

This example creates a new message channel and uses one of the ports to send a message, which will be received by the other port, and then explicitly starts sending the message.

``` js
var msgChannel = new MessageChannel();
msgChannel.port1.postMessage('Hello world');
msgChannel.port1.start();
```

## <span>Notes</span>

The **start** method is called implicitly by when an event handler function is assigned to the **onmessage** property. In Internet Explorer 10, the start method is also called implicitly when a message event is registered using the **addEventListener** method.

## <span>Related specifications</span>

[W3C Web Messaging Specification](http://www.w3.org/TR/webmessaging/)
:   W3C Candidate Recommendation
