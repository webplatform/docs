---
title: 'postMessage'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/web-messaging/MessagePort
    href: /apis/web-messaging/MessagePort
standardization_status: 'W3C Candidate Recommendation'
summary: 'Posts a message through the channel, from one port to the other.'
tags:
  0: API
  1: Object
  2: Methods
  4: Web
  5: Messaging
uri: apis/web-messaging/MessagePort/postMessage

---
## Summary

Posts a message through the channel, from one port to the other.

Method of [apis/web-messaging/MessagePort](/apis/web-messaging/MessagePort)[apis/web-messaging/MessagePort](/apis/web-messaging/MessagePort)

## Syntax

``` js
 MessagePort.postMessage(message, transfer);
```

## Parameters

### message

 Data-type
:   any

 JavaScript primitive, such as a **string**, **PixelArray**, **ImageData**, **Blob**, **File**, or **ArrayBuffer**.

### transfer

 Data-type
:   any

(Optional)

Objects listed in *transfer* are transferred, not just cloned, meaning that they are no longer usable on the sending side. Throws a *DataCloneError* if *transfer* array contains duplicate objects or the source or target ports, or if *message* could not be cloned.

## Return Value

No return value

## Examples

This example creates a new message channel and uses one of the ports to send a message, which will be received by the other port.

``` js
var msgChannel = new MessageChannel();
msgChannel.port1.postMessage('Hello world');
```

## Notes

When you create a new **MessageChannel** object, it has two connected **MessagePort** objects that can only send and receive messages between them. If the *ports* parameter is supplied but contains errors, an **InvalidStateError** exception is thrown. Sending a message containing an un-supported object (such as a function), a **DataCloneError** exception is thrown.

## Related specifications

[W3C Web Messaging Specification](http://www.w3.org/TR/webmessaging/)
:   W3C Candidate Recommendation
