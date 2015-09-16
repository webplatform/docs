---
title: load
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary and compat and better spec links'
readiness: 'In Progress'
standardization_status: 'W3C Recommendation'
tags:
  - Events
uri: dom/Element/load

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

The following example shows how to declare an **onload** event for a document that is designed to work with multiple browsers and earlier versions of Internet Explorer.

``` html
<!doctype html>
<head>
  <title>Load Event Sample</title>
  <script type="text/javascript">
  function doLoad() {
     alert( "The load event is executing" );
  }
  if ( window.addEventListener ) {
     window.addEventListener( "load", doLoad, false );
  }
  else
     if ( window.attachEvent ) {
        window.attachEvent( "onload", doLoad );
  } else
        if ( window.onLoad ) {
           window.onload = doLoad;
  }
  </script>
</head>
<body>
  <h1>Load Event Sample</h1>
  <p>This sample demonstrates how to execute
     an event while the document is loading.</p>
</body>
</html>
```

## Notes

### Remarks

The client loads applications, embedded objects, and images as soon as it encounters the **applet**, **embed**, and **img** objects during parsing. Consequently, the **onload** event for these objects occurs before the client parses any subsequent objects. To ensure that an event handler receives the **onload** event for these objects, place the **script** object that defines the event handler before the object and use the **onload** attribute in the object to set the handler. The **onload** attribute of the **body** object sets an **onload** event handler for the **window**. This technique of calling the window **onload** event through the **body** object is overridden by any other means of invoking the window **onload** event, provided the handlers are in the same script language. Loads the object for which the event is specified. To invoke this event, do one of the following:

-   Open a document to invoke this event for the document or any object within it.

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
-   **HTMLDocumentEvents4**
-   **HTMLElementEvents4**

### Syntax

### Standards information

-   [HTML 4.01 Specification](http://go.microsoft.com/fwlink/p/?linkid=25320), Section 18.2.3

### Event handler parameters

*pEvtObj* [in]
:   Type: ****IHTMLEventObj****

