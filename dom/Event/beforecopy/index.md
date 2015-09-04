---
title: beforecopy
tags:
  - Events
readiness: 'In Progress'
notes:
  - 'Needs summary, spec, and compat'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onbeforecopyEX.htm'
uri: dom/Event/beforecopy

---
# beforecopy

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

This example uses the **onbeforecopy** event to customize copy behavior.

    <HEAD>
    <SCRIPT>
    var sNewValue = "copy event fired";
    var bFired = false;
    var sSave = "";
    function Source_Beforecopy()
    {
      sSave = oSource.innerText;
      bFired = true;
      event.returnValue = false;
    }
    function Source_Copy()
    {
      window.clipboardData.setData("Text", sNewValue);
    }
    function Target_BeforePaste()
    {
      event.returnValue = false;
    }
    function Target_Paste()
    {
      event.returnValue = false;
      oTarget.value = window.clipboardData.getData("Text");
    }
    </SCRIPT>
    </HEAD>
    <BODY>
    <SPAN ID=oSource onbeforecopy="Source_Beforecopy()"
           oncopy="Source_Copy()">copy this text</SPAN>
    <INPUT ID=oTarget onbeforepaste="Target_BeforePaste()"
           onpaste="Target_Paste()">
    </BODY>

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onbeforecopyEX.htm)

## Notes

### Remarks

The **onbeforecopy** event fires on the source element. Use the [**setData**](/dom/DataTransfer/setData) method to specify a data format for the selection. None. To invoke this event, do one of the following:

-   Right-click to display the shortcut menu and select Copy.
-   Or press CTRL+C.

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

