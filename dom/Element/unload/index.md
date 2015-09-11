---
title: unload
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onunloadEX.htm'
notes:
  - 'Needs summary, and compat, also better spec link'
readiness: 'In Progress'
standardization_status: 'W3C Recommendation'
tags:
  - Events
uri: dom/Element/unload

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
</td>
</tr>
</table>
## <span>Examples</span>

This example shows how to use the **onunload** event to run script when the window object has been unloaded.

``` html
<head>
<script type="text/javascript" for="window" event="onunload">
    alert("The onunload event fired for the window object.");
</script>
<script type="text/javascript">
    function fnRelocate()
    {
    location.href="/workshop/samples/author/dhtml/refs/onunloadEX_target.htm";
    }
</script>
</head>
<body>
<input type="button" value="Go To Page 2" onclick="fnRelocate()">
</body>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onunloadEX.htm)

## <span>Notes</span>

### <span>Remarks</span>

If you call **window**.[**open**](/dom/Window/open) from this event, the Pop-up Blocker feature in Microsoft Internet Explorer 6 prevents the pop-up window from appearing. Removes the object or document from the browser window. To invoke this event, do one of the following:

-   Close the current window.
-   Navigate to another location by entering a new address or selecting a Favorite.
-   Click the Back, Forward, Refresh, or Home button.
-   Click an [**anchor**](/html/elements/a) that refers the browser to another document.
-   Invoke the [**anchor**](/html/elements/a).[**click**](/dom/HTMLElement/click) method.
-   Invoke the [**Document**](/dom/Document).[**write**](/dom/Document/write) method.
-   Invoke the [**Document**](/dom/Document).[**open**](/dom/Document/open) method.
-   Invoke the [**Document**](/dom/Document).[**close**](/dom/Document/close) method.
-   Invoke the **window**.[**close**](/dom/Window/close) method.
-   Invoke the **window**.[**open**](/dom/Window/open) method, providing the possible value **\_self** for the window name.
-   Invoke the [**location**](/dom/Location).[**replace**](/dom/Location/replace) method.
-   Invoke the [**location**](/dom/Location).[**reload**](/dom/Location/reload) method.
-   Specify a new value for the [**location**](/dom/Location).[**href**](/dom/Location/href) property.
-   Submit a **form** to the address specified in the **ACTION** attribute via the **INPUT type=submit** control, or invoke the **form**.[**submit**](/dom/HTMLFormElement/submit) method.

For security reasons, the **unload** event does not open modeless dialog boxes, such as those created with the [**alert**](/dom/Window/alert) method. This changes affects webpages displayed in IE9 Standards mode or later document modes. The *pEvtObj* parameter is required for the following interfaces:

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

### <span>Standards information</span>

-   [HTML 4.01 Specification](http://go.microsoft.com/fwlink/p/?linkid=25320), Section 18.2.3

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `body`
-   `frameSet`
-   `Window`
-   `Reference`
-   `Conceptual`
-   `About the Pop-up Blocker`
