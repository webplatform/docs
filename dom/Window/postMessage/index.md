---
title: postMessage
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Sends a cross-document message.'
uri: dom/Window/postMessage

---
# postMessage

## Summary

Sends a cross-document message.

*Method of [dom/Window](/dom/Window)*

## Syntax

``` {.js}
 targetFrame.postMessage(/* see parameter list */);
```

## Parameters

### msg

 Data-typeÂ
:   String

 A **String** that contains the message data.

### targetOrigin

 Data-typeÂ
:   String

 A **Variant** of type **String** that specifies a target URI.

## Return Value

No return value

## Examples

If Document A (on [http://127.0.0.1](http://127.0.0.1)) contains a reference to the [**contentWindow**](/dom/HTMLIFrameElement/contentWindow) property of Document B (on <http://localhost>), script in Document A can send a message to Document B by calling the **postMessage** method as follows:

``` {.js}
var targetframe = document.getElementsByTagName('iframe')[0];
targetframe.contentWindow.postMessage('Hello World','http://localhost');
```

The script in Document B can respond to the message by registering the [**onmessage**](/dom/Window/message) event handler for incoming messages.

``` {.js}
window.addEventListener('message',function(e) {
    if (e.origin == 'http://127.0.0.1') {
        if (e.data == 'Hello World') {
            // We can reply with this
            e.source.postMessage('Hello');
        } else {
            console.log(e);
        }
    }
},false);
```

## Notes

**Security Warning:Â Â **While "\*" is a valid value for *targetOrigin*, set the parameter to the value you expected to receive; otherwise, the security of your message might be compromised. For more information about this security message, see Section 3.1.2 of the [HTML5 Web Messaging](http://go.microsoft.com/fwlink/?LinkId=199803) Specification (Editor's Draft) from the World Wide Web Consortium (W3C). The **postMessage** method allows cooperative text exchange between untrusted modules from different domains embedded within a page. It does so by ensuring a consistent and secure process for text-based data exchange. When a script invokes this method on a **window** object, the browser sends an [**onmessage**](/dom/Window/message) event to the target document on which the **data** property has been set to the value passed in *msg*. When a target URI is passed into the method, it must have at least a protocol and a host specified. The message will only be sent if the target window has the same protocol and host as the specified target URI. The **postMessage** method call does not return until the event listeners of the target document have finished executing.

### Standards information

-   [HTML5 Web Messaging](http://go.microsoft.com/fwlink/p/?linkid=199803), Section 5.3

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[postMessage](https://developer.mozilla.org/en-US/docs/Web/API/Window.postMessage) Article]

Portions of this content come from the Microsoft Developer Network: [[postMessage Method](http://msdn.microsoft.com/en-us/library/ie/cc197015(v=vs.85).aspx) Article]

