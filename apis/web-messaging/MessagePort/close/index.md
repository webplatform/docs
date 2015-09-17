---
title: 'close'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/web-messaging/MessagePort
    href: /apis/web-messaging/MessagePort
standardization_status: 'W3C Candidate Recommendation'
summary: 'Disconnects the port, so that it is no longer active.'
tags:
  - API_Object_Methods
  - API
  - Web_Messaging
uri: apis/web-messaging/MessagePort/close

---
## Summary

Disconnects the port, so that it is no longer active.

Method of [apis/web-messaging/MessagePort](/apis/web-messaging/MessagePort)[apis/web-messaging/MessagePort](/apis/web-messaging/MessagePort)

## Syntax

``` js
 MessagePort.close();
```

## Return Value

No return value

## Examples

This example creates a new message channel and uses one of the ports to send a message, which will be received by the other port, then closes the port.

``` js
var msgChannel = new MessageChannel();
msgChannel.port1.postMessage('Hello world');
msgChannel.port1.close();
```

## Notes

This method releases the **MessagePort** from its corresponding **MessagePort**. After calling the **close** method, message events will no longer be received on this port and **postMessage** will no longer post any messages. To continue messaging, you need to create a new **MessageChannel** and resend one of the ports to the other window or document.

## Related specifications

[W3C Web Messaging Specification](http://www.w3.org/TR/webmessaging/)
:   W3C Candidate Recommendation
