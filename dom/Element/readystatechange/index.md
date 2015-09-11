---
title: readystatechange
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary, spec, and compat'
readiness: 'In Progress'
tags:
  - Events
uri: dom/Element/readystatechange

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

## <span>Overview Table</span>

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
## <span>Examples</span>

This example uses the **onreadystatechange** event to invoke a function when the [**readyState**](/dom/Element/readyState) is complete.

``` html
document.onreadystatechange=fnStartInit;
function fnStartInit()
{
   if (document.readyState=="complete")
   {
      // Finish initialization.
   }
}
```

## <span>Notes</span>

### <span>Remarks</span>

You can use the [**readyState**](/dom/Element/readyState) property to query the current state of the element when the **onreadystatechange** event fires. All elements expose an **onreadystatechange** event. The following objects always fire the event because they load data: **applet**, [**Document**](/dom/Document), **frame**, **frameSet**, **iframe**, **img**, **link**, **object**, **script**, and **xml** elements. Other objects will only fire the **onreadystatechange** event when a DHTML Behavior is attached. When working with behaviors, wait for the **onreadystatechange** event to fire and verify that the **readyState** property of the element is set to **complete** to ensure that the behavior is completely downloaded and applied to the element. Until the **onreadystatechange** event fires, if you use any of the behavior-defined members before attaching the behavior to the element, a scripting error can result, indicating that the object does not support that particular property or method. Signals the ready state of the document. To invoke this event, do one of the following:

-   Change the ready state.

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

### <span>Syntax</span>

### <span>Standards information</span>

There are no standards that apply here.

### <span>Event handler parameters</span>

*pEvtObj* [in]
:   Type: ****IHTMLEventObj****

