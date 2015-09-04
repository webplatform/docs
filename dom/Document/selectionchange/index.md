---
title: selectionchange
tags:
  - Events
readiness: 'Not Ready'
notes:
  - 'Needs summary, examples, specs, compat'
uri: dom/Document/selectionchange

---
# selectionchange

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

To invoke this event, do one of the following:

-   Cause the [**selection**](/dom/Selection) object's **type** property to change.
-   Return a range from a different location when using the [**createRange**](/dom/Selection/createRange) method of the [**selection**](/dom/Selection) object.
-   Move the insertion point in an editable region of the document using the mouse or keyboard.
-   Refresh the page when an editable region has focus.
-   Start or extend a *text selection* by dragging the mouse or using SHIFT+an arrow key.
-   Make a *control selection* in an editable region of the document.
-   Add or remove an element from a multiple selection by pressing SHIFT while clicking on the element.
-   Delete text or an element in an editable region of the document by using the BACKSPACE key, DELETE key, CTRL+X, or the Delete command.
-   Insert text or an element in an editable region of the document by using CTRL+V or the Paste command.

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

## See also

### Related pages (MSDN)

-   `Modifying Documents in Edit Mode`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

