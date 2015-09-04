---
title: getClientRects
tags:
  - API
  - Object
  - Methods
  - CSS
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'A collection of ClientRect objects, one for each CSS border box associated with the element. Each ClientRect object contains read-only left, top, right, and bottom properties describing the border box, relative to the top-left of the viewport. For tables with captions, the caption is included even though it is outside the border box of the table.'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/rectselection.htm'
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/rectdemo.htm'
uri: dom/HTMLElement/getClientRects

---
# getClientRects

## Summary

A collection of ClientRect objects, one for each CSS border box associated with the element. Each ClientRect object contains read-only left, top, right, and bottom properties describing the border box, relative to the top-left of the viewport. For tables with captions, the caption is included even though it is outside the border box of the table.

*Method of [dom/HTMLElement](/dom/HTMLElement)*

## Syntax

``` {.js}
var rectList = element.getClientRects();
```

## Return Value

Returns an object of type ClientRectList.

A **ClientRectList** collection, that contains **ClientRect** objects with the following properties -

     top: Number
     left: Number
     right: Number
     bottom: Number
     height: Number
     width: Number

## Examples

This example uses the **getClientRects** and [**getBoundingClientRect**](/dom/HTMLElement/getBoundingClientRect) methods to highlight text lines in an object.

``` {.html}
<head>
<script>
var rcts;
var keyCount=0;
function Highlight(obj) {
    rcts = obj.getClientRects();
    rctLength= rcts.length;
    if (keyCount > rctLength-1) {
        idBeige.style.display="none";
        keyCount = 0
    }
    // set the rendering properties for the yellow DIV
    cdRight = rcts[keyCount].right + idBody.scrollLeft;
    cdLeft = rcts[keyCount].left + idBody.scrollLeft;
    cdTop = rcts[keyCount].top + idBody.scrollTop;
    cdBottom = rcts[keyCount].bottom + idBody.scrollTop;
    idYellow.style.top = cdTop;
    idYellow.style.width = (cdRight-cdLeft) - 5;
    idYellow.style.display = 'inline';
    // set the rendering properties for the beige DIV
    bndRight = obj.getBoundingClientRect().right +
        idBody.scrollLeft;
    bndLeft = obj.getBoundingClientRect().left +
        idBody.scrollLeft;
    bndTop = obj.getBoundingClientRect().top +
        idBody.scrollTop;
    idBeige.style.top = bndTop;
    idBeige.style.width = (bndRight-bndLeft) - 5;
    idBeige.style.height = cdTop - bndTop;
    if (keyCount>0){
        idBeige.style.display = 'inline';
    }
    keyCount++;
}
</script>
</head>
<body id="idBody">
<div id="oID_1" onclick="Highlight(this)"
    onkeydown="Highlight(this)">
A large block of text should go here. Click this
block of text multiple times to see each line
highlight with every click of the mouse button.
Once each line has been highlighted, the process
begins again starting with the first line.
</div>
<div style="position:absolute; left:5; top:400;
z-index:-1; background-color:yellow; display:none"
ID="idYellow"></div>
<div style="position:absolute; left:5; top:400;
z-index:-1; background-color:beige; display:none"
ID="idBeige"></div>
</body>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/rectselection.htm)

This example uses the [**ClientRect**](/css/cssom/ClientRect) collection with the **getClientRects** and [**getBoundingClientRect**](/dom/HTMLElement/getBoundingClientRect) methods to determine the position of the text rectangle within an element. In each line, the left-justified text does not extend to the right margin of the box that contains the text. Using the collection, you can determine the coordinates of the rectangle that surrounds only the content in each line. The example code reads these rectangle coordinates and instructs the ball to move over the text only, and not to the end of the line.

``` {.html}
<head>
<script>
var timid = -1;
var timoID_2 = -1;
var nLine;
var nPosInLine;
var oRcts;
var nDivLen;
var nEraser;
function LoadDone() {
    oTextRange = document.body.createTextRange();
    // Get bounding rect of the range
    oRcts = oTextRange.getClientRects();
    nLine = 0;
    oBndRct = obj.getBoundingClientRect();
    nDivLen = oBndRct.right - oBndRct.left + 1;
    MoveTo();
}
function MoveTo() {
    if (nLine >= oRcts.length) {
        nLine = 0;
    }
    obj.style.top = oRcts[nLine].top;
    nPosInLine = oRcts[nLine].left;
    nEraser = 0;
    timoID_2 = setInterval("MoveToInLine()",60);
}
function MoveToInLine() {
    if (nPosInLine >= oRcts[nLine].right - nDivLen) {
        clearInterval(timoID_2);
        timoID_2 = -1;
        obj.style.left = oRcts[nLine].right - nDivLen;
        nLine++;
        timid = setTimeout("MoveTo()", 100);
        return;
    }
    if (nEraser == 0) {
        nEraser = 1;
    }
    else {
        nEraser = 0;
    }
    im.src = "/workshop/graphics/dot.png";
    obj.style.left = nPosInLine;
    nPosInLine += 3;
}
function End() {
    if(timid != -1) {
        clearInterval(timid);
        timid = -1;
    }
    if(timoID_2 != -1) {
        clearInterval(timoID_2);
        timoID_2 = -1;
    }
}
</script>
</head>
<body id="bodyid" onload="LoadDone()"
    onresize="End();LoadDone();" onunload="End()">
<p style="text-align:center">
<b>The quick brown fox jumps over the lazy dog.</b>
</p>
<div id="obj" style="position:absolute">
<img id="im" src="/workshop/graphics/dot.png"
    border=0 height=16 width=16>
</div>
</body>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/rectdemo.htm)

## Notes

-   Before being in the process of standardization, it was intended that this method would return a TextRectangle object for each line of text in an element. However, the CSSOM working draft specifies that it returns a ClientRect for each border box. For an inline element, the two definitions are the same. But for a block element, the CSSOM version returns only a single rectangle.
-   The amount of scrolling that has been done of the viewport area (or any other scrollable element) is taken into account when computing the rectangles.
-   The returned rectangles do not include the bounds of any child elements that might happen to overflow.
-   For HTML AREA elements, SVG elements that do not render anything themselves, display:none elements, and generally any elements that are not directly rendered, an empty list is returned.
-   Rectangles are returned even for CSS boxes that have empty border-boxes. The left, top, right and bottom coordinates can still be meaningful.
-   Fractional pixel offsets are possible.

### Compatibility notes

Internet Explorer 8 and below - **getClientRect** returns a proprietary `TextRectangle` object. While it is similar to [ClientRect](/css/cssom/ClientRect), it does not have `height` or `width` properties and furthermore cannot have any additional properties (including `height` and `width`) added to it.

## Related specifications

Specification
:   Status
[CSSOM View Module](http://www.w3.org/TR/cssom-view/#dom-range-getclientrects)
:   Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/DOM/element.getClientRects)

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

