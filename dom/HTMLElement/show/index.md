---
title: show
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'In Progress'
notes:
  - 'summary, clean-up MSDN import'
uri: dom/HTMLElement/show

---
# show

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

*Method of [dom/HTMLElement](/dom/HTMLElement)*

## Syntax

``` {.js}
var object = object.show(x, y, w, h, pElement);
```

## Parameters

### x

 Data-typeÂ
:   any

### y

 Data-typeÂ
:   any

### w

 Data-typeÂ
:   any

### h

 Data-typeÂ
:   any

### pElement

 Data-typeÂ
:   VARIANT

## Return Value

Returns an object of type DOM Node.

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

## Examples

The following example shows how to use the **show** method to create and display a pop-up window.

    <html>
    <head>
    <SCRIPT LANGUAGE="JScript">
    var oPopup = window.createPopup();
    function window_onload() {
        var oPopupBody = oPopup.document.body;
        oPopupBody.style.backgroundColor = "lightyellow";
        oPopupBody.style.border = "solid black 1px";
        oPopupBody.innerHTML = "Display some <B>HTML</B> here.";
        oPopup.show(100, 100, 200, 50, document.body);}
    </SCRIPT>
    </head>
    <body onload="window_onload();">
    </body>
    </html>

## Notes

### Remarks

A **popup** object is set to the same zoom level as the parent window. Windows Internet ExplorerÂ 8. Pop-up windows zoom by default; this behavior cannot be changed.

### Syntax

### Standards information

There are no standards that apply here.

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

