---
title: filterchange
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/filters.htm'
notes:
  - 'Needs summary, spec reference, standardization status'
readiness: 'In Progress'
tags:
  - Events
uri: dom/Event/filterchange

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

This example uses the **onfilterchange** event to trigger a filter effect. When the document loads, the block of text is erased using a checkerboard-down Transition. Once the checkerboard Transition is complete, the image is made visible using a box-in Transition.

``` html
<HTML>
<HEAD>
<TITLE>Microsoft Cascading Style Sheet Controls Samples</TITLE>
</HEAD>
<body>
<h2>Some text filters out (checkerboard), and at its completion
an image filters in (box-in).  Refresh repeats.</h2>
<Div ID="TextRegion" STYLE="Position: absolute; border: solid red;
    background-color: lightblue; LEFT: 0; TOP: 100; WIDTH: 100%;
    VISIBILITY: visible; FILTER: revealTrans(Transition = 11,
    Duration = 1.25)">
Text that will filter upon document load.<br>
Text that will filter upon document load.<br>
Text that will filter upon document load.<br>
Text that will filter upon document load.<br>
Text that will filter upon document load.<br>
Text that will filter upon document load.<br>
Text that will filter upon document load.
</DIV>
<DIV ID="ImageRegion" STYLE="Position: absolute; border: solid red;
    LEFT: 0; TOP: 100; WIDTH: 30%; VISIBILITY: hidden;
    FILTER: revealTrans(Transition = 0, Duration = 1.25)">
<IMAGE id=image1 SRC="/workshop/samples/author/graphics/dhtml/blupan.png">
</DIV>
<SCRIPT LANGUAGE=VBScript>
Sub Window_onload
    Call TextRegion.filters.revealTrans.Apply ()
    Call ImageRegion.filters.revealTrans.Apply()
    Call Start
End Sub
Sub Start
   TextRegion.style.visibility = "hidden"
   ImageRegion.style.visibility = "visible"
   Call TextRegion.filters.revealTrans.Play()
End Sub
Sub TextRegion_onfilterchange
   if TextRegion.filters.revealTrans.Status = 0 then
      Call ImageRegion.filters.revealTrans.Play(1.5)
   End If
End Sub
</SCRIPT>
</BODY>
</HTML>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/filters.htm)

## Notes

### Remarks

Signals that the filter on an object has changed state. To invoke this event, do one of the following:

-   Change the filter state.

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

