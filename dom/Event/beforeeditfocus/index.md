---
title: beforeeditfocus
tags:
  - Events
  - DOM
readiness: 'Not Ready'
notes:
  - 'Needs summary, examples, spec, and compat'
uri: dom/Event/beforeeditfocus

---
# beforeeditfocus

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

For the **onbeforeeditfocus** event to fire, document elements must be in edit mode. One way to invoke edit mode is to set the [**designMode**](/dom/Document/designMode) property to **On**. The **onbeforeeditfocus** event differs from the [**onfocus**](/dom/HTMLElement/focus) event. The **onbeforeeditfocus** event fires before an object enters a *UI Activation* state, whereas the **onfocus** event fires when an object has focus. **Note**  This event also fires when an **input** or **textArea** object gets the focus in browse mode. As of Microsoft Internet Explorer 5.5, Web authors can also set the [**contentEditable**](/html/attributes/contentEditable) attribute to **true** on the body element, and if necessary, to specific elements in the body, to invoke edit mode. Moves the object into a *UI Activation* state. To invoke this event, do one of the following:

-   Press the ENTER key or click an object when it has focus.
-   Double-click an object.

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

