---
title: 'setActive'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/setActive.htm'
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/setActive_2.htm'
notes:
  - 'summary, clean-up of MSDN import'
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
uri: dom/HTMLElement/setActive

---
Method of [dom/HTMLElement](/dom/HTMLElement)[dom/HTMLElement](/dom/HTMLElement)

## Syntax

``` js
var object = object.setActive();
```

## Return Value

Returns an object of type DOM NodeDOM Node

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

## Examples

This example demonstrates how to use the **setActive** method between **frame**s.

``` html
...
<SCRIPT>
function fnBottomActive(){
    //Set the object with ID=btnLarger active in frame with ID=oFrame1.
    window.parent.oFrame1.secondButton.setActive();
}
</SCRIPT>
...
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/setActive.htm)

This example demonstrates how to use the **setActive** method between windows. By clicking the **SetActive** button in the left window, the method sets the **Second Button** as the active object in the right window, although the object does not receive focus. The object receives focus when its page receives focus. To confirm that the object is active, click the right window's title bar. The button appears to be selected.

``` html
<HTML>
<HEAD>
<SCRIPT>
function fnOpen(){
    //Open new window.
    oWin1 = window.open("/workshop/samples/author/dhtml/refs/setactive_content.htm",
        "oWin1",
        "top=10px,left=480px,height=375px,width=200px,resizable=1");
    //Set focus back to the parent window.
    this.focus();
}
function fnBottomActive(){
    //Set the object with ID=btnLarger active in the other window.
    window.parent.oWin1.secondButton.setActive();
}
</SCRIPT>
</HEAD>
<BODY onload="fnOpen();">
<CENTER>
<TABLE border="1">
<TR><TD>
    <BUTTON id="btn1" onclick="fnBottomActive();">Set Active</BUTTON></TD></TR>
</TABLE>
</CENTER>
</BODY>
</HTML>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/setActive_2.htm)

## Notes

### Remarks

The **setActive** method does not cause the document to scroll to the active object in the current page or in another **frame** or **window**.

### Syntax

### Standards information

There are no standards that apply here.
