---
title: 'blur'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onblurEX.htm'
notes:
  - 'Needs summary, spec reference, standardization status'
readiness: 'In Progress'
tags:
  - Events
  - DOM
  - Needs_Summary
uri: dom/FocusEvent/blur

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
## Examples

This example shows how to display the name of the object that has lost focus, that is, the object that fires the **onblur** event.

``` js
<html>
<body>
<input type="text"
    name="txtFName"
    value="First Name"
    onblur="console.log(event.srcElement.name)">
<input type="text"
    name="txtLName"
    value="Last Name"
    onblur="console.log(event.srcElement.name)">
<input type="text"
    name="txtPhone"
    value="Phone"
    onblur="console.log(event.srcElement.name)">
</body>
</html>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onblurEX.htm)

## Notes

### Remarks

The **onblur** event fires on the original object before the [**onfocus**](/dom/FocusEvent/focus) or [**onclick**](/dom/HTMLElement/click) event fires on the object that is receiving focus. Where applicable, the **onblur** event fires after the [**onchange**](/dom/Element/change) event. Use the focus events to determine when to prepare an object to receive or validate input from the user. As of Microsoft Internet Explorer 5, you must set the [**tabIndex**](/html/attributes/tabIndex) attribute of elements that expose the **onblur** event. For Internet Explorer 5 and later, the **onblur** event is asynchronous. Switches focus away from the object on which the event is fired. To invoke this event, do one of the following:

-   Click the mouse on the document background or another control.
-   Use the keyboard to navigate from one object to the next.
-   Invoke the **blur** method when an object has focus.
-   Switch focus to a different application or open a second window.

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
-   **HTMLDocumentEvents4**

### Syntax

### Standards information

-   [HTML 4.01 Specification](http://go.microsoft.com/fwlink/p/?linkid=25320), Section 18.2.3

### Event handler parameters

*pEvtObj* [in]
:   Type: ****IHTMLEventObj****
