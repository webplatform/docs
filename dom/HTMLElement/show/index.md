---
title: 'show'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'summary, clean-up MSDN import'
readiness: 'In Progress'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/HTMLElement
    href: /dom/HTMLElement
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/HTMLElement
tags:
  - API_Object_Methods
  - DOM
  - Needs_Summary
uri: dom/HTMLElement/show

---
Method of [dom/HTMLElement](/dom/HTMLElement)[dom/HTMLElement](/dom/HTMLElement)

## Syntax

``` js
var object = object.show(x, y, w, h, pElement);
```

## Parameters

### x

 Data-type
:   any

### y

 Data-type
:   any

### w

 Data-type
:   any

### h

 Data-type
:   any

### pElement

 Data-type
:   VARIANT

## Return Value

Returns an object of type DOM NodeDOM Node

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

## Examples

The following example shows how to use the **show** method to create and display a pop-up window.

``` html
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
```

## Notes

### Remarks

A **popup** object is set to the same zoom level as the parent window. Windows Internet Explorer 8. Pop-up windows zoom by default; this behavior cannot be changed.

### Syntax

### Standards information

There are no standards that apply here.
