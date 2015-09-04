---
title: movestart
tags:
  - Events
readiness: 'In Progress'
notes:
  - 'Needs summary, spec, and compat'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onmovestartendEx1.htm'
uri: dom/Element/movestart

---
# movestart

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

The following example shows how to use the **onmovestart** event with a movable **DIV** and have the background color and inner text change when the **DIV** starts to move.

    <HTML>
    <HEAD>
    <TITLE>Editing events sample page</TITLE>
    <SCRIPT>
    // Turn on 2-D positioning
    document.execCommand("2D-position",false,true);
    // Function called when the onmovestart event is fired
    function fnHandleMoveStart() {
      var oDiv = event.srcElement
      oDiv.style.backgroundColor = "green";
      oDiv.innerText = "I Started Moving";
    }
    function fnHandleMoveEnd() {
      var oDiv = event.srcElement
      oDiv.style.backgroundColor = "red";
      oDiv.innerText = "I Stopped";
    }
    </SCRIPT>
    </HEAD>
    <BODY  onmovestart="fnHandleMoveStart();" onmoveend="fnHandleMoveEnd();">
    <DIV CONTENTEDITABLE="true">
    <DIV style="width:300px;height:100px; color:white; background-color:red;
    position:absolute;">
    My DIV</DIV>
    </DIV>
    </BODY>
    </HTML>

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onmovestartendEx1.htm)

## Notes

### Remarks

The **onmovestart** event fires only when an editable element starts to move. This event can only be bound to absolutely positioned elements. Calls the associated event handler if there is one. To invoke this event, do one of the following:

-   Start to move the editable object.

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

