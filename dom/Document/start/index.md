---
title: 'start'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onstartEX.htm'
notes:
  - "\nDeletion Candidate:   Content has no standard and is only for a deprecated element (marquee.) No real use being documented now or in the future since it isn't on any track to be a standard.\n\n\n\nNeeds summary and compat"
readiness: 'In Progress'
standardization_status: Non-Standard
tags:
  - Events
uri: dom/Document/start

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

This example shows how to use the **onstart** event on a **marquee**.

``` html
<BODY>
<P>An alert dialog box displays each time the onstart event fires.
<MARQUEE onstart="alert('onstart fired')"
         BEHAVIOR=alernate LOOP=2>Marquee Text</MARQUEE>
</BODY>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onstartEX.htm)

## Notes

### Remarks

The **start** method does not cause the **onstart** event to fire. Initiates the next loop of the **marquee** contents. To invoke this event, do one of the following:

-   Set the [**LOOP**](/html/attributes/loop) attribute to 1 or higher.
-   Omit the [**LOOP**](/html/attributes/loop) attribute so that the **marquee** loops indefinitely.

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

## See also

### Related pages

-   `marquee`
-   `Reference`
-   `behavior`
-   loop[loop](/html/attributes/loop)
-   finish[finish](/dom/Event/finish)
