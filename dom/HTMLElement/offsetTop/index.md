---
title: offsetTop
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'In Progress'
notes:
  - 'summary, clean-up of MSDN import'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/offsetTop.htm'
uri: dom/HTMLElement/offsetTop

---
# offsetTop

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/HTMLElement](/dom/HTMLElement)</span></span>

## Syntax

``` {.js}
var result = element.offsetTop;
element.offsetTop = value;
```

## Examples

This example uses the **offsetTop** property to determine whether an object is in the user's view.

    <html>

    <head>
    <script type="text/javascript">
    function isinView(oObject)
    {
        var oParent = oObject.offsetParent;
        var iOffsetTop = oObject.offsetTop;
        var iClientHeight = oParent.clientHeight;
        if (iOffsetTop > iClientHeight) {
            alert("Special Text not in view. Expand Window to put Text in View.");
        }
        else{
             alert("Special Text in View!");
        }
    }
    </script>
    </head>

    <body onload="window.resizeTo(430,250)" onclick="isinView(oID_1)" scroll="NO">

    <div style="position: absolute; left: 20px">
        Click anywhere in window to see if special text is in view.</div>
    <div id="oID_1" style="position: absolute;
        left: 50px;
        top: 300px;
        width: 280px;
        color: silver;
        font-size: large;
        font-weight: bold;
        background-color: aqua;
        font-family: Arial">
        Here&#39;s some special text </div>

    </body>

    </html>

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/offsetTop.htm)

## Notes

### Remarks

You can determine the location, width, and height of an object by using a combination of the [**offsetLeft**](/dom/HTMLElement/offsetLeft), **offsetTop**, [**offsetHeight**](/dom/HTMLElement/offsetHeight), and [**offsetWidth**](/dom/HTMLElement/offsetWidth) properties. These numeric properties specify the physical coordinates and dimensions of the object relative to the object's offset parent. For more information about how to access the dimension and location of objects on the page through the Dynamic HTML (DHTML) Document Object Model (DOM), see Measuring Element Dimension and Location with CSSOM in Internet Explorer 9.

### Syntax

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

