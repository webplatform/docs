---
title: 'message'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs compat and better spec link'
readiness: 'Almost Ready'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Fires when a message is received from another context (frame, window, worker and similar).'
tags:
  - Events
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/MessageEvent/data2
uri: dom/Window/message

---
## Summary

Fires when a message is received from another context (frame, window, worker and similar).

## Overview Table

<table class="wikitable">
<tr>
<th>
Synchronous

</th>
<td>
No

</td>
</tr>
<tr>
<th>
Bubbles

</th>
<td>
No

</td>
</tr>
<tr>
<th>
Target

</th>
<td>
dom/Window

</td>
</tr>
<tr>
<th>
Cancelable

</th>
<td>
No

</td>
</tr>
<tr>
<th>
Default action

</th>
<td>
</td>
</tr>
</table>
## Examples

For example, if document A contains a reference to the [**contentWindow**](/dom/HTMLIFrameElement/contentWindow) of document B, script in document A can send document B a message by calling [**postMessage**](/dom/Window/postMessage) as follows:

``` html
var o = document.getElementsByTagName('iframe')[0];
o.contentWindow.postMessage('Hello World');
```

The script in document B can respond to the message by registering the **onmessage** event handler for incoming messages.

``` html
window.attachEvent('onmessage',function(e) {
    if (e.domain == 'example.com') {
        if (e.data == 'Hello World') {
            e.source.postMessage('Hello');
        } else {
            alert(e.data);
        }
    }
});
```

## Notes

For info on channel messaging with [**Workers**](/apis/workers/Worker), see [**MessagePort**](/apis/web-messaging/MessagePort) and [**MessageChannel**](/apis/web-messaging/MessageChannel). The **onmessage** event is fired when script invokes [**postMessage**](/dom/Window/postMessage) on a **window** object to send the target document a message. The [**data**](/w/index.php?title=dom/MessageEvent/data2&action=edit&redlink=1) property of the incoming event is set to the value passed in **postMessage**. **Security Warning:  **For best results, check the [**origin**](/dom/MessageEvent/origin) attribute to ensure that messages are only accepted from domains that you expect. For more information, see Section 7.4.2 of the [HTML5 (Working Draft)](http://go.microsoft.com/fwlink/?linkid=203771) specification from the World Wide Web Consortium (W3C). To invoke this event, do one of the following:

-   Send a cross-document message with **postMessage**.
-   Send a message to a **Worker** with **postMessage**.

The *pEvtObj* parameter is required for the following interfaces:

-   **HTMLWindowEvents3**
-   [**MessagePort**](/apis/web-messaging/MessagePort)

### Standards information

-   [HTML5 Web Messaging](http://go.microsoft.com/fwlink/p/?linkid=199803), Section 5.3

