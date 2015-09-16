---
title: 'beforecut'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onbeforecutEX.htm'
notes:
  - 'Needs summary, spec, and compat'
readiness: 'In Progress'
tags:
  - Events
  - DOM
uri: dom/Event/beforecut

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

This example uses the [**setData**](/dom/DataTransfer/setData) and [**getData**](/dom/DataTransfer/getData) methods with the [**ClipboardData**](/dom/ClipboardData) object to perform a cut-and-paste operation through the shortcut menu.

``` html
<head>
<script>
var sSave = "";
function fnBeforeCut() {
   event.returnValue = false;
}
function fnCut() {
   event.returnValue = false;
   sSave = oSource.innerText;
   oSource.innerText = "";
}
function fnBeforePaste() {
   event.returnValue = false;
}
function fnPaste() {
   event.returnValue = false;
   oTarget.innerText = sSave;
}
</script>
</head>
<body>
<div id="oSource" class="selectandcut"
    onbeforecut="fnBeforeCut()"
    oncut="fnCut()">Select and Cut this Text
</div>
<br>
<br>
<div id="oTarget" class="pastehere"
    onbeforepaste="fnBeforePaste()"
    onpaste="fnPaste()">Paste the Text Here
</div>
</body>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onbeforecutEX.htm)

## Notes

### Remarks

Creating custom code for cutting requires several steps:

1.  Set **event.returnValue=false** in the **onbeforecut** event to enable the Cut shortcut menu item.
2.  Specify a data format in which to transfer the selection through the [**setData**](/dom/DataTransfer/setData) method.
3.  Invoke the [**setData**](/dom/DataTransfer/setData) method in the [**oncut**](/dom/Event/cut) event.

None. To invoke this event, do one of the following:

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
