---
title: 'beforeactivate'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary, examples, spec, and compat'
readiness: 'Not Ready'
tags:
  - Events
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/methods/setActive
    - dom/methods/focus
    - dom/properties/activeElement
    - dom/properties/fromElement2
    - dom/events/activate
    - dom/events/beforedeactivate
    - dom/events/deactivate
    - dom/events/focusin
    - dom/events/focusout
uri: dom/Event/beforeactivate

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

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
dom/Element

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
 ?

</td>
</tr>
</table>
**Needs Examples**: This section should include examples.

## Notes

### Remarks

Each document may have up to one active element. Set the active element with the [**setActive**](/w/index.php?title=dom/methods/setActive&action=edit&redlink=1) or [**focus**](/w/index.php?title=dom/methods/focus&action=edit&redlink=1) methods. Using the **setActive** method has no effect on document focus. Using the **focus** method on an individual element causes the element to gain focus and become the active element. Using the [**focus**](/w/index.php?title=dom/methods/focus&action=edit&redlink=1) method on a document that does not have the focus moves the document to the front of the display. Additionally, the document's active element gains focus. For a given display, only one element has focus at any given time. Striking a key directly affects only the element with focus. Events fired by that keystroke may be scripted to affect other documents and child elements. With Microsoft Internet Explorer 5.5 and later, focus on a [**Document**](/dom/Document), and the [**active element**](/w/index.php?title=dom/properties/activeElement&action=edit&redlink=1) of a **document** can be managed separately. With Microsoft Internet Explorer 6 and later, use the **onbeforeactivate** event to cancel setting an element as active. Canceling an element's **onbeforeactivate** event has three different behaviors, depending on the action which fired the event.

-   When fired by a user clicking on the element, canceling will force the [**focus**](/w/index.php?title=dom/methods/focus&action=edit&redlink=1) on the parent element and bubble up the chain until it hits a focusable element.
-   When fired by a user tabbing through the document, canceling will force the [**focus**](/w/index.php?title=dom/methods/focus&action=edit&redlink=1) on the next element in the taborder. Shift-tab will force the **focus** on the previous element in the taborder.
-   When fired programmatically by the [**focus**](/w/index.php?title=dom/methods/focus&action=edit&redlink=1) or the document.[**setActive**](/w/index.php?title=dom/methods/setActive&action=edit&redlink=1) methods, canceling will have no effect.

**Note**  The **onbeforeactivate** event cannot be canceled when fired programmatically. Change activation from the **event**.[**fromElement**](/w/index.php?title=dom/properties/fromElement2&action=edit&redlink=1) to the **event**.**srcElement**. To invoke this event, do one of the following:

-   Click an element, other than the [**active**](/w/index.php?title=dom/properties/activeElement&action=edit&redlink=1) element of the document.
-   Use the keyboard to move focus from the active element to another element.
-   Invoke the [**setActive**](/w/index.php?title=dom/methods/setActive&action=edit&redlink=1) method on an element, when the element is not the active element.
-   Invoke the [**focus**](/w/index.php?title=dom/methods/focus&action=edit&redlink=1) method on an element, when the element is not the active element.

The *pEvtObj* parameter is required for the following interfaces:

-   **HTMLFrameSiteEvents2**
-   **HTMLElementEvents**
-   **HTMLElementEvents2**
-   **HTMLLinkElementEvents**
-   **HTMLLinkElementEvents2**
-   **HTMLFormElementEvents**
-   **HTMLFormElementEvents2**
-   **HTMLImgEvents**
-   **HTMLImgEvents2**
-   **HTMLTextContainerEvents**
-   **HTMLTextContainerEvents2**
-   **HTMLAnchorEvents2**
-   **HTMLLabelEvents**
-   **HTMLLabelEvents2**
-   **HTMLSelectElementEvents**
-   **HTMLSelectElementEvents2**
-   **HTMLInputTextElementEvents**
-   **HTMLInputTextElementEvents2**
-   **HTMLOptionButtonElementEvents**
-   **HTMLOptionButtonElementEvents2**
-   **HTMLButtonElementEvents**
-   **HTMLButtonElementEvents2**
-   **HTMLMarqueeElementEvents**
-   **HTMLMarqueeElementEvents2**
-   **HTMLControlElementEvents**
-   **HTMLControlElementEvents2**
-   **HTMLMapEvents**
-   **HTMLMapEvents2**
-   **HTMLAreaEvents**
-   **HTMLAreaEvents2**
-   **HTMLTableEvents**
-   **HTMLTableEvents2**
-   **HTMLScriptEvents**
-   **HTMLScriptEvents2**
-   **HTMLStyleElementEvents**
-   **HTMLStyleElementEvents2**
-   **HTMLInputFileElementEvents**
-   **HTMLInputFileElementEvents2**
-   **HTMLInputImageEvents**
-   **HTMLInputImageEvents2**
-   **HTMLDocumentEvents**

### Syntax

### Standards information

There are no standards that apply here.

### Event handler parameters

*pEvtObj* [in]
:   Type: ****IHTMLEventObj****

## See also

### Related pages

-   a[a](/html/elements/a)
-   `address`
-   `applet`
-   `area`
-   `b`
-   `bdo`
-   `big`
-   `blockQuote`
-   `body`
-   `button`
-   `caption`
-   `center`
-   `cite`
-   `code`
-   `custom`
-   `dd`
-   `dfn`
-   `dir`
-   `div`
-   `dl`
-   Document[Document](/dom/Document)
-   `dt`
-   `em`
-   `embed`
-   `fieldSet`
-   `font`
-   `form`
-   `hn`
-   `hr`
-   `i`
-   `img`
-   `input type=button`
-   `input type=checkbox`
-   `input type=file`
-   `input type=image`
-   `input type=reset`
-   `input type=password`
-   `input type=radio`
-   `input type=submit`
-   `input type=text`
-   `kbd`
-   `label`
-   `legend`
-   `li`
-   `listing`
-   `map`
-   `marquee`
-   `menu`
-   nextID[nextID](/html/elements/nextID)
-   `noBR`
-   `ol`
-   `p`
-   `plainText`
-   `pre`
-   `rt`
-   `ruby`
-   `s`
-   `samp`
-   `select`
-   `small`
-   `span`
-   `strike`
-   `strong`
-   `sub`
-   `sup`
-   table[table](/html/elements/table)
-   `tBody`
-   `td`
-   `textArea`
-   `tFoot`
-   `th`
-   `tHead`
-   `tr`
-   `tt`
-   `u`
-   `ul`
-   `var`
-   `xmp`
-   `Reference`
-   onactivate[onactivate](/w/index.php?title=dom/events/activate&action=edit&redlink=1)
-   onbeforedeactivate[onbeforedeactivate](/w/index.php?title=dom/events/beforedeactivate&action=edit&redlink=1)
-   ondeactivate[ondeactivate](/w/index.php?title=dom/events/deactivate&action=edit&redlink=1)
-   onfocusin[onfocusin](/w/index.php?title=dom/events/focusin&action=edit&redlink=1)
-   onfocusout[onfocusout](/w/index.php?title=dom/events/focusout&action=edit&redlink=1)
