---
title: 'paste'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onbeforecutEX.htm'
notes:
  - 'Needs summary, spec, and compat'
readiness: 'In Progress'
tags:
  - Events
uri: dom/Element/paste

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

This example uses the [**ClipboardData**](/dom/ClipboardData) object to implement custom editing functionality.

``` html
<HEAD>
<SCRIPT>
var sNewString = "new content associated with this object";
var sSave = "";
// Selects the text that is to be cut.
function fnLoad() {
    var r = document.body.createTextRange();
    r.findText(oSource.innerText);
    r.select();
}
// Stores the text of the SPAN in a variable that is set
// to an empty string in the variable declaration above.
function fnBeforeCut() {
    sSave = oSource.innerText;
    event.returnValue = false;
}
// Associates the variable sNewString with the text being cut.
function fnCut() {
    window.clipboardData.setData("Text", sNewString);
}
function fnBeforePaste() {
    event.returnValue = false;
}
// The second parameter set in getData causes sNewString
// to be pasted into the text input. Passing no second
// parameter causes the SPAN text to be pasted instead.
function fnPaste() {
    event.returnValue = false;
    oTarget.value = window.clipboardData.getData("Text", sNewString);
}
</SCRIPT>
</HEAD>
<BODY onload="fnLoad()">
<SPAN ID="oSource"
      onbeforecut="fnBeforeCut()"
      oncut="fnCut()">Cut this Text</SPAN>
<INPUT ID="oTarget" TYPE="text" VALUE="Paste the Text Here"
      onbeforepaste="fnBeforePaste()"
      onpaste="fnPaste()">
</BODY>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onbeforecutEX.htm)

## Notes

### Remarks

Creating custom code to enable the Paste command requires several steps.

1.  Set the event object [**returnValue**](/dom/BeforeUnloadEvent/returnValue) to false in the [**onbeforepaste**](/dom/Event/beforepaste) event to enable the Paste shortcut menu item.
2.  Cancel the default behavior of the client by setting the event object **returnValue** to false in the **onpaste** event handler. This applies only to objects, such as the **text box**, that have a default behavior defined for them.
3.  Specify a data format in which to paste the selection through the [**getData**](/dom/DataTransfer/getData) method.
4.  Invoke the method in the **onpaste** event to execute custom paste code.

Inserts the data from the system clipboard into the specified location on the document. To invoke this event, do one of the following:

-   Right-click to display the shortcut menu and select Paste.
-   Or press CTRL+V.

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

