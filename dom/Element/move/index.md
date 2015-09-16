---
title: 'move'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onmoveEx1.htm'
notes:
  - 'Needs summary, spec, and compat'
readiness: 'In Progress'
tags:
  - Events
uri: dom/Element/move

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
## Examples

The following example shows how to use the **onmove** event and display the x and y coordinates of a **DIV** as it is moved.

``` html
<html>
<head>
<title>The onmove event</title>
<script>
// Turn on 2-D positioning
document.execCommand("2D-position",false,true);
function fnHandleMove() {
  oXDelta.innerText = event.srcElement.offsetLeft;
  oYDelta.innerText = event.srcElement.offsetTop;
}
</script>
</head>
<body onmove="fnHandleMove();">
<b>Current Object:</b><br>
X delta: <span id="oXDelta">n/a</span><br>
Y delta: <span id="oYDelta">n/a</span><br>
<div contenteditable="true">
<div style="width:300px;height:100px; background-color:red; position:absolute;">
Movable DIV</div>
</div>
</body>
</html>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onmoveEx1.htm)

## Notes

### Remarks

This event can be bound to relatively positioned elements as well as absolutely positioned elements. This event does not fire when it is bound to an object inside a container object that moves. Calls the associated event handler if there is one. To invoke this event, do one of the following:

-   Change the absolute position of the object.

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

