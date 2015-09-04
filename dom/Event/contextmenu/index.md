---
title: contextmenu
tags:
  - Events
  - DOM
readiness: 'In Progress'
notes:
  - 'Needs summary, spec, and compat'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/oncontextmenu.htm'
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/oncontextmenuEX1.htm'
uri: dom/Event/contextmenu

---
# contextmenu

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

This example shows how to prevent a context menu from appearing by canceling the **oncontextmenu** event handler.

    <span style="width: 300px; background-color: blue; color: white;"
        oncontextmenu="return false">
    The context menu never displays when you right-click in this box. </span>

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/oncontextmenu.htm)

Although **area** elements inherit the **oncontextmenu** event by way of the object hierarchy, they do not respond to right-click events in Internet Explorer. However, it is possible to imitate the desired behavior by using the [**onfocus**](/dom/HTMLElement/focus) and [**onblur**](/dom/HTMLElement/blur) events to determine the currently selected region and trigger the appropriate action in the context menu handler of the **img** itself. Although it isn't used by Internet Explorer, retain the **oncontextmenu** event attribute on the **area** elements for a fully cross-client implementation.

    <script type="text/javascript">
    var selectedArea = null;
    function activate(e,f) {
        selectedArea = f ? e : null;
    }
    function menu(e) {
        if (selectedArea)
            alert('right-click: ' + selectedArea.id);
        else {
            // cross-client case
            if (e.tagName == 'AREA')
                alert('right-click: ' + e.id);
            else
                alert('right-click: ' + e.tagName);
        }
        return false;
    }
    </script>
    <map id="Map0">
    <area id="Area1" onfocus="activate(this,true)" onblur="activate(this,false)"
        oncontextmenu="return menu(this)" shape="rect" coords="100, 50, 200, 150" href="..."/>
    </map>
    <img src="..." oncontextmenu="return menu(this)" usemap="#Map0" />

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/oncontextmenuEX1.htm)

## Notes

### Remarks

Opens the context menu. To cancel the default behavior, set the [**returnValue**](/dom/BeforeUnloadEvent/returnValue) property of the **event** object to **false**. To invoke this event, do one of the following:

-   Right-click the object.

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

