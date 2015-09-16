---
title: reset
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onreset.htm'
notes:
  - 'Needs summary and compat'
readiness: 'In Progress'
standardization_status: 'W3C Recommendation'
tags:
  - Events
uri: dom/Element/reset

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

This example demonstrates how to use the **onreset** event for a **form** object. Reset the form by clicking the first or second button. The only difference between the two buttons is that the second button invokes the [**reset**](/dom/HTMLFormElement/reset) method and the first button is of **input type=reset**. When either button is pressed the **form** is reset, resulting in the **onreset** event call on the **form** object. The **onreset** event calls an event handler which in turn adds the text `Resetting form.` to the text area below.

``` html
<HTML>
<HEAD>
<SCRIPT>
function doReset(){
    oTextArea1.innerText += "Resetting form.  ";
}
</SCRIPT>
</HEAD>
<BODY>
<FORM name="form1" onreset="doReset();"
    <B>Form</B><BR>
    style="border:2px solid #cccccc; background:#EEEEEE; padding:10px; ">
    <b>Enter some text:</b>
    <INPUT type="text" name="oText1" value=""><BR><BR>
    <INPUT TYPE="reset" value="Input type=reset"/>
    <BUTTON onclick="form.reset();">form.reset()</BUTTON>
</FORM>
<B>Form status</B><BR>
<SPAN id="oTextArea1" ></SPAN>
<BR><BR>
<BUTTON onclick="location.reload(true);">Refresh Page</BUTTON>
</BODY>
</HTML>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onreset.htm)

## Notes

### Remarks

Executes associated code. To invoke this event, do one of the following:

-   Click an **input type=reset** button.
-   Invoke the [**reset**](/dom/HTMLFormElement/reset) method.

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

