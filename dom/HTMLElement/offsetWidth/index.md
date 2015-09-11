---
title: offsetWidth
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/offsetWidth.htm'
notes:
  - 'summary, clean-up of MSDN import'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/HTMLElement
    href: /dom/HTMLElement
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/HTMLElement/offsetWidth

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Property of [dom/HTMLElement](/dom/HTMLElement)[dom/HTMLElement](/dom/HTMLElement)

## <span>Syntax</span>

``` js
var result = element.offsetWidth;
element.offsetWidth = value;
```

## <span>Examples</span>

This example adjusts the size of a clock's readout to fit the current width and height of the document.

``` html
<HTML>
<HEAD><TITLE>A Simple Clock</TITLE>
<SCRIPT LANGUAGE="JScript">
function startClock()
{
    window.setInterval("Clock_Tick()", 1000);
    Clock_Tick();
}

var ratio = 4;
function Clock_Tick()
{
    var s = Date();
    var t = s.substring(11,19);
    var doc_height = document.body.offsetHeight;
    var doc_width = document.body.offsetWidth;

    if ((doc_height*ratio)>doc_width)
        doc_height = doc_width / ratio;
        document.all.MyTime.innerText = t;
        document.all.MyTime.style.fontSize = doc_height;
}
</SCRIPT>
<BODY onload="startClock()">
<P ID="MyTime">&nbsp;</P>
</BODY>
</HTML>
```

This example uses the **offsetWidth** property and the [**clientWidth**](/dom/HTMLElement/clientWidth) property to show the different ways of measuring the object size.

``` html
<DIV ID=oDiv STYLE="overflow:scroll; width:200; height:100"> . . . </DIV>
<BUTTON onclick="alert(oDiv.clientWidth)">client width</BUTTON>
<BUTTON onclick="alert(oDiv.offsetWidth)">offset width</BUTTON>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/offsetWidth.htm)

## <span>Notes</span>

### <span>Remarks</span>

You can determine the location, width, and height of an object by using a combination of the [**offsetLeft**](/dom/HTMLElement/offsetLeft), [**offsetTop**](/dom/HTMLElement/offsetTop), [**offsetHeight**](/dom/HTMLElement/offsetHeight), and **offsetWidth** properties. These numeric properties specify the physical coordinates and dimensions of the object relative to the object's offset parent. For more information about how to access the dimension and location of objects on the page through the Dynamic HTML (DHTML) Document Object Model (DOM), see Measuring Element Dimension and Location with CSSOM in Internet Explorer 9. To comply with the [Cascading Style Sheets, Level 1 (CSS1)](http://go.microsoft.com/fwlink/p/?linkid=203774) box model, Microsoft Internet Explorer 6 and later calculate the height of objects differently when you use the [!DOCTYPE](/html/elements/!DOCTYPE) declaration in your document to switch on standards-compliant mode. This difference may affect the value of the **offsetWidth** propety. When standards-compliant mode is switched on, the [**width**](/css/properties/width) property specifies the distance between the left and right edges of the bounding box that surrounds the object's content. When standards-compliant mode is not switched on, and with earlier versions of Windows Internet Explorer, the **width** property also includes the [**border**](/css/properties/border) and [**padding**](/css/properties/padding) belts that surround the object's bounding box. For more information, see CSS Enhancements in Internet Explorer 6.

### <span>Syntax</span>