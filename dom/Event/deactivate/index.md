---
title: deactivate
tags:
  - Events
  - DOM
readiness: 'In Progress'
notes:
  - 'Needs example, spec reference, standardization status'
summary: 'Sets an active version of an object to not active.'
uri: dom/Event/deactivate

---
# deactivate

## Summary

Sets an active version of an object to not active.

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

**Note**  When focus leaves the document, the active element does not change and the [**onbeforedeactivate**](/dom/Event/beforedeactivate) event will not fire. Each document may have up to one active element. Set the active element with the [**setActive**](/dom/HTMLElement/setActive) or [**focus**](/dom/HTMLElement/focus) methods. Using the **setActive** method has no effect on document focus. Using the **focus** method on an individual element causes the element to gain focus and become the active element. Using the [**focus**](/dom/HTMLElement/focus) method on a document that does not have the focus moves the document to the front of the display. Additionally, the document's active element gains focus. For a given display, only one element has focus at any given time. Striking a key directly affects only the element with focus. Events fired by that keystroke may be scripted to affect other documents and child elements. For Microsoft Internet Explorer 6 and later, the **event**.**toElement** property is now exposed by the **ondeactivate** event. With Microsoft Internet Explorer 5.5 and later, focus on a [**Document**](/dom/Document), and the [**active element**](/dom/Document/activeElement) of a **document** can be managed separately. Use the **ondeactivate** event to manage formatting changes when a element loses activation. Change activation from the **event**.**srcElement** to the **event**.**toElement**. To invoke this event, do one of the following:

-   Click an element, other than the [**active**](/dom/Document/activeElement) element of the document.
-   Use the keyboard to move focus from the active element to another element.
-   Invoke the [**setActive**](/dom/HTMLElement/setActive) method on an element, when the element is not the active element.

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

