---
title: 'focusout'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary, example, spec reference, standardization status'
readiness: 'In Progress'
tags:
  - Events
  - DOM
  - Needs_Summary
  - Needs_Examples
uri: dom/FocusEvent/focusout

---
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
## Notes

### Remarks

Each document may have up to one active element. Set the active element with the [**setActive**](/dom/HTMLElement/setActive) or [**focus**](/dom/FocusEvent/focus) methods. Using the **setActive** method has no effect on document focus. Using the **focus** method on an individual element causes the element to gain focus and become the active element, and this causes **onfocusout** to fire for this active element. Using the [**focus**](/dom/FocusEvent/focus) method on a document that does not have the focus moves the document to the front of the display. Additionally, the document's active element gains focus, and this causes **onfocusout** to fire for this active element. For a given display, only one element has focus at any given time. Striking a key directly affects only the element with focus. Events fired by that keystroke may be scripted to affect other documents and child elements. With Microsoft Internet Explorer 5.5 and later, focus on a [**Document**](/dom/Document) and the [**active element**](/dom/Document/activeElement) of a **document** can be managed separately. Use the **onfocusout** event to manage formatting changes when an element loses focus. To invoke this event, do one of the following:

-   Click a [**Document**](/dom/Document), when the **document** does not have focus.
-   Click an element, other than the current element with focus.
-   Use the keyboard to move focus from the active element to another element.
-   Invoke the [**focus**](/dom/FocusEvent/focus) method on an element, when the element is not the active element.

### Syntax

### Standards information

There are no standards that apply here.

### Event handler parameters

*pEvtObj* [in]
:   Type: ****IHTMLEventObj****
