---
title: 'resize'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary, examples, spec, and compat'
readiness: 'Not Ready'
tags:
  - Events
  - Needs_Summary
  - Needs_Examples
uri: dom/Element/resize

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

The **onresize** event fires for block and inline objects with layout, even if document or CSS (cascading style sheets) property values are changed. Objects have layout when measurements such as the [**height**](/css/properties/height) and [**width**](/css/properties/width) attributes are set, or when the [**position**](/css/properties/position) of the object is set. Intrinsic objects, such as **button**, and windowed objects, such as **window** and **iframe**, fire as expected. This event does not fire for files with embedded controls. Resizing HTML applications also fires the **onresize** event. No default action. To invoke this event, do one of the following:

-   Change the height or width of the object.

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

#### window.onresize events in Metro style apps using JavaScript

In Metro style apps using JavaScript, the **window.onresize** event fires when the screen keyboard is shown and when the app's viewport is resized. You can use the **window.innerHeight**, **window.innerWidth**, **window.pageXOffset**, and **window.pageYOffset** style properties to determine the size and location of the new viewport.

### Syntax

### Standards information

There are no standards that apply here.

### Event handler parameters

*pEvtObj* [in]
:   Type: ****IHTMLEventObj****

