---
title: 'cut'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs example, spec reference, standardization status'
readiness: 'In Progress'
summary: 'Fires after a data selection is cut to the clipboard.'
tags:
  - Events
  - DOM
  - Needs_Examples
uri: dom/Event/cut

---
## Summary

Fires after a data selection is cut to the clipboard.

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

Creating custom code for cutting requires several steps:

1.  Set **event.returnValue=false** in the [**onbeforecut**](/dom/Event/beforecut) event to enable the Cut shortcut menu item.
2.  Specify a data format in which to transfer the selection through the [**setData**](/dom/DataTransfer/setData) method.
3.  Invoke the [**setData**](/dom/DataTransfer/setData) method in the **oncut** event.

Set **event.returnValue=false** in the **oncut** event handler to cancel the default action. The default action must be canceled to successfully use the [**setData**](/dom/DataTransfer/setData) method. Web authors can use the [**innerHTML**](/dom/HTMLElement/innerHTML) property or the [**createRange**](/dom/Selection/createRange) method to perform the cut operation once the event is canceled. Removes the selection from the document and persists it in the clipboard. To invoke this event, do one of the following:

-   Right-click to display the shortcut menu and select Cut.
-   Or press CTRL+X if the selection is within a text field.

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
