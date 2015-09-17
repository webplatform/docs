---
title: 'doScroll'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/doScrollEX.htm'
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/doScrollEX1.htm'
notes:
  - 'summary, examples best practices, compatibility, standards, clean-up of MSDN sections'
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
uri: dom/HTMLElement/doScroll

---
Method of [dom/HTMLElement](/dom/HTMLElement)[dom/HTMLElement](/dom/HTMLElement)

## Syntax

``` js
var object = object.doScroll(/* see parameter list */);
```

## Parameters

### component

 Data-type
:   VARIANT

 A **String** that specifies how the object scrolls, using one of the following values.

## Return Value

Returns an object of type DOM NodeDOM Node

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

## Examples

The following example uses the **doScroll** method to scroll down when a button is clicked.

``` html
<HEAD>
<SCRIPT>
function scrollBehavior()
{
document.body.doScroll("scrollbarPageRight");
}
function scrollBehavior1()
{
txtScrollMe.doScroll("scrollbarDown");
}
function scrollBehavior2()
{
txtScrollMe.doScroll("scrollbarPageDown");
}
</SCRIPT>
</HEAD>
<BODY>
<BUTTON
   onclick="scrollBehavior()"
   CLASS="colorIt"
>
Click to Scroll Page
</BUTTON>
<BR>
<HR>
<BUTTON
   onclick="scrollBehavior1()"
   ondblclick="scrollBehavior2()"
   CLASS="colorIt">
   Click to Scroll Text Area
</BUTTON><BR><BR>
<TEXTAREA ID=txtScrollMe CLASS="colorIt">
    This text area scrolls down when
    the "Click to Scroll the Text
    Area" button is clicked. The doScroll
    method scrolls it as if the down
    arrow component of the scroll bar
    had been clicked. Double-click the
    button to scroll down a whole page.
</BODY>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/doScrollEX.htm)

The following example uses the **doScroll** method to scroll down a text area in one-second intervals.

``` html
<HEAD>
<SCRIPT>
var iTimer;
function timeIt()
{
iTimer = setInterval("scrollIt()", 1000);
}
function scrollIt()
{
oScrollMe.doScroll("down");
}
</SCRIPT>
</HEAD>
<BODY onload="timeIt()">
<DIV ID=oScrollMe STYLE="width:200px;height:75px;overflow:scroll">
</DIV>
</BODY>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/doScrollEX1.htm)

## Notes

### Remarks

As of Windows Internet Explorer 9, this method is supported only for webpages displayed in IE5 (Quirks) mode. For webpages displayed in standards mode (preferred), use the [**scrollLeft**](/dom/HTMLElement/scrollLeft) and [**scrollTop**](/dom/HTMLElement/scrollTop) properties. The **doScroll** method is available on all objects, regardless of whether they support scrollbars. Cascading Style Sheets (CSS) allow you to scroll on all objects through the [**overflow**](/css/properties/overflow) property. When the content of an element changes and causes scroll bars to display, the **doScroll** method might not work correctly immediately following the content update. When this happens, you can use the [**setTimeout**](/dom/Window/setTimeout) method to enable the browser to recognize the dynamic changes that affect scrolling.

### Syntax

### Standards information

There are no standards that apply here.
