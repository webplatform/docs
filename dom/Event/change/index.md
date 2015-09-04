---
title: change
tags:
  - Events
  - DOM
readiness: 'In Progress'
notes:
  - 'Needs summary, spec, and compat'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onchangeEX.htm'
uri: dom/Event/change

---
# change

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

This example uses the **onchange** event to retrieve the selected option of a **select** object.

    <body>
    <form>
      <p>Select a different option in the drop-down list box to trigger the onchange event.
      <select name="selTest" onchange="alert('Index: ' + this.selectedIndex
         + '\nValue: ' + this.options[this.selectedIndex].value)">
      <option value="Books">Books</option>
      <option value="Clothing">Clothing</option>
      <option value="Housewares">Housewares</option>
      </select> </p>
    </form>
    </body>

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onchangeEX.htm)

## Notes

### Remarks

This event is fired when the contents are committed and not while the value is changing. For example, on a text box, this event is not fired while the user is typing, but rather when the user commits the change by leaving the text box that has focus. In addition, this event is executed before the code specified by [**onblur**](/dom/HTMLElement/blur) when the control is also losing the focus. The **onchange** event does not fire when the selected option of the **select** object is changed programmatically. Changed text selection is committed. To invoke this event, do one of the following:

-   Choose a different **option** in a **select** object using mouse or keyboard navigation.
-   Alter text in the text area and then navigate out of the object.

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

-   [HTML 4.01 Specification](http://go.microsoft.com/fwlink/p/?linkid=25320), Section 18.2.3

### Event handler parameters

*pEvtObj* [in]
:   Type: ****IHTMLEventObj****

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

