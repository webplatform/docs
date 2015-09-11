---
title: activate
attributions:
  - 'Microsoft Developer Network: [[active Event](http://msdn.microsoft.com/en-us/library/ie/ms536787(v=vs.85).aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onactivate.htm'
readiness: 'Ready to Use'
standardization_status: Non-Standard
summary: 'Fires when the object is set as the active element.'
tags:
  - Events
  - DOM
uri: dom/UIEvent/activate

---
## <span>Summary</span>

Fires when the object is set as the active element.

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
Yes

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
see Notes

</td>
</tr>
</table>
## <span>Examples</span>

The following example demonstrates the order of event firing for the **onactivate** and **onload** events. As each event fires, it appends a string to the **div** element within the document. The **onactivate** event fires before the **onload** event.

``` html
<!DOCTYPE html>
<html>
<head>
<script type="text/javascript">
function fnActivate(){
    oDIV1.innerHTML += "<br/><br/>The <b>onactivate</b> event, available as of
        Internet Explorer 5.5, fires first on the body element.";
}
function fnLoad(){
    oDIV1.innerHTML += "<br/><br/>The <b>onload</b> event, available as of
        Internet Explorer 4.0, fires after the <i>onactivate</i> event fires
        on the body element.";
}
</script>
</head>
<body onactivate="fnActivate();" onload="fnLoad();">
<div id="oDIV1"></div>
</body>
</html>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onactivate.htm)

## <span>Notes</span>

### <span>Remarks</span>

**Note**  Using the [**setActive**](/dom/HTMLElement/setActive) method has no effect on document focus. Using the [**focus**](/dom/HTMLElement/focus) method on an individual element causes the element to gain focus and become the active element. When one object loses activation and another object becomes the [**activeElement**](/dom/Document/activeElement), the **onfocus** event fires on the object becoming the **activeElement** only after the [**onblur**](/dom/HTMLElement/blur) event fires on the object losing activation. Each document may have up to one active element. Set the active element with the **setActive** or **focus** methods. Using the **focus** method on a document that does not have the focus moves the document to the front of the display. Additionally, the document's active element gains focus. The **onactivate** event fires before the **onload** event for any of the objects listed in the Applies To section. For Microsoft Internet Explorer 6 and later, the **event.fromElement** property is now exposed by this event. For Microsoft Internet Explorer 5.5 and later, focus on a [**Document**](/dom/Document), and the **activeElement** of a **Document** can be managed separately. Use the **onactivate** event to manage formatting changes when an element is made active. Change activation from the **event.fromElement** to the **event.srcElement**. To invoke this event, do one of the following:

-   Click an element other than the **activeElement** element of the document.
-   Use the keyboard to move focus from the active element to another element.
-   Invoke the **setActive** method on an element, when the element is not the active element.

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
