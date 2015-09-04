---
title: losecapture
tags:
  - Events
readiness: 'In Progress'
notes:
  - 'needs summary, spec, and compat'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onlosecaptureEX.htm'
uri: dom/Element/losecapture

---
# losecapture

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

## Overview Table

Synchronous
:   No
Bubbles
:   No
Target
:   dom/Element
Cancelable
:   No
Default action
:    ?

## Examples

This example shows how to fire the **onlosecapture** event. When the user clicks the mouse, the [**releaseCapture**](/dom/Document/releaseCapture) method is invoked and subsequently fires the **onlosecapture** event.

    <BODY onload="divOwnCapture.setCapture()"
        onclick="divOwnCapture.releaseCapture();">
    <DIV ID=divOwnCapture
        onmousemove="txtWriteLocation.value=event.clientX
            + event.clientY";
        onlosecapture="alert(event.srcElement.id
            + ' lost mouse capture.')">
    <P>Mouse capture has been set to this gray division (DIV) at
       load time using the setCapture method. The text area will track
       the mousemove event anywhere in the document.<BR><BR>
    <TEXTAREA ID=txtWriteLocation COLS=2></TEXTAREA>
    </DIV>
    <HR>
    <DIV ID=divNoCapture>
    <P>Click anywhere on the document to invoke the releaseCapture
       method, whereby the onlosecapture event will fire.</P>
    </DIV>
    </BODY>

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onlosecaptureEX.htm)

## Notes

### Remarks

Sends the event notification to the object that is losing the mouse capture. To invoke this event, do one of the following:

-   Set mouse capture to a different object.
-   Change the active window so that the current document using mouse capture loses focus.
-   Invoke the [**releaseCapture**](/dom/Document/releaseCapture) method on the [**Document**](/dom/Document) or object.

The *pEvtObj* parameter is required for the following interfaces:

-   **HTMLAnchorEvents2**
-   **HTMLAreaEvents2**
-   **HTMLButtonElementEvents2**
-   **HTMLControlElementEvents2**
-   **HTMLDocumentEvents2**
-   **HTMLElementEvents2**
-   **HTMLFormElementEvents2**
-   **HTMLImgEvents2**
-   **HTMLFrameSiteEvents2**
-   **HTMLInputFileElementEvents2**
-   **HTMLInputImageEvents2**
-   **HTMLInputTextElementEvents2**
-   **HTMLLabelEvents2**
-   **HTMLLinkElementEvents2**
-   **HTMLMapEvents2**
-   **HTMLMarqueeElementEvents2**
-   **HTMLObjectElementEvents2**
-   **HTMLOptionButtonElementEvents2**
-   **HTMLScriptEvents2**
-   **HTMLSelectElementEvents2**
-   **HTMLStyleElementEvents2**
-   **HTMLTableEvents2**
-   **HTMLTextContainerEvents2**
-   **HTMLWindowEvents2**

### Syntax

### Standards information

There are no standards that apply here.

### Event handler parameters

*pEvtObj* [in]
:   Type: ****IHTMLEventObj****

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

