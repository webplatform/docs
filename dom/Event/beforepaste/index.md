---
title: beforepaste
tags:
  - Events
  - DOM
readiness: 'Not Ready'
notes:
  - 'Needs summary, examples, spec, and compat'
uri: dom/Event/beforepaste

---
# beforepaste

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

**Needs Examples**: This section should include examples.

## Notes

### Remarks

Creating custom code for pasting requires several steps:

1.  Set **event.returnValue=false** in the **onbeforepaste** event to enable the Paste shortcut menu item.
2.  Cancel the default behavior of the client by including **event.returnValue=false** in the [**onpaste**](/dom/Element/paste) event handler. This guideline applies only to objects, such as the **text box**, that have a defined default behavior.
3.  Specify a data format in which to paste the selection through the [**getData**](/dom/DataTransfer/getData) method.
4.  Invoke the [**getData**](/dom/DataTransfer/getData) method in the [**onpaste**](/dom/Element/paste) event to execute custom code for pasting.

None. To invoke this event, do one of the following:

-   Right-click to display the shortcut menu and select Paste.
-   Or press CTRL+V.

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

