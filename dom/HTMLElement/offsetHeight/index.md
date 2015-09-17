---
title: 'offsetHeight'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/offsetHeight.htm'
notes:
  - 'summary, clean-up of MSDN import'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/HTMLElement
    href: /dom/HTMLElement
tags:
  - API_Object_Properties
  - DOM
  - Needs_Summary
uri: dom/HTMLElement/offsetHeight

---
Property of [dom/HTMLElement](/dom/HTMLElement)[dom/HTMLElement](/dom/HTMLElement)

## Syntax

``` js
var result = element.offsetHeight;
element.offsetHeight = value;
```

## Examples

This example adjusts the size of a clock's readout to fit the current width and height of the document body.

``` html
<HTML>
<HEAD>
<TITLE>A Simple Clock</TITLE>
<SCRIPT LANGUAGE="JScript">
function startClock()
{
    window.setInterval("Clock_Tick()", 1000);
    Clock_Tick();
}

var iRatio = 4;
function Clock_Tick()
{
    var dToday = Date();
    var sTime = dToday.substring(11,19);
    var iDocHeight = document.body.offsetHeight;
    var iDocWidth = document.body.offsetWidth;

    if ((iDocHeight*iRatio)>iDocWidth)
        iDocHeight = iDocWidth / iRatio;
    document.all.MyTime.innerText = sTime;
    document.all.MyTime.style.fontSize = iDocHeight;
}
</SCRIPT>
</HEAD>
<BODY onload="startClock()">
<P ID="MyTime">&nbsp;</P>
</BODY>
</HTML>
```

This example uses the **offsetHeight** property and the [**clientHeight**](/dom/HTMLElement/clientHeight) property to show different ways of measuring the object size.

``` html
<DIV ID=oDiv STYLE="overflow:scroll; width:200; height:100"> . . . </DIV>
<BUTTON onclick="alert(oDiv.clientHeight)">client height</BUTTON>
<BUTTON onclick="alert(oDiv.offsetHeight)">offset height</BUTTON>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/offsetHeight.htm)

## Notes

### Remarks

You can determine the location, width, and height of an object by using a combination of the [**offsetLeft**](/dom/HTMLElement/offsetLeft), [**offsetTop**](/dom/HTMLElement/offsetTop), **offsetHeight**, and [**offsetWidth**](/dom/HTMLElement/offsetWidth) properties. These numeric properties specify the physical coordinates and dimensions of the object relative to the object's offset parent. For more information about how to access the dimension and location of elements on the page through the Dynamic HTML (DHTML) Document Object Model (DOM), see Measuring Element Dimension and Location with CSSOM in Internet Explorer 9. To comply with the [Cascading Style Sheets, Level 1 (CSS1)](http://go.microsoft.com/fwlink/p/?linkid=203774) box model, Microsoft Internet Explorer 6 and later calculate the height of objects differently when you use the [!DOCTYPE](/html/elements/!DOCTYPE) declaration in your document to switch on standards-compliant mode. This difference may affect the value of the **offsetHeight** property. When standards-compliant mode is switched on, the [**height**](/css/properties/height) property specifies the distance between the top and bottom edges of the bounding box that surrounds the object's content. When standards-compliant mode is not switched on, and with earlier versions of Windows Internet Explorer, the **height** property also includes the [**border**](/css/properties/border) and [**padding**](/css/properties/padding) belts that surround the object's bounding box. For more information, see CSS Enhancements in Internet Explorer 6.

### Syntax
