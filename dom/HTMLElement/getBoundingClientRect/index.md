---
title: getBoundingClientRect
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/DOM/element.getBoundingClientRect)'
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/rectselection.htm'
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/rectdemo.htm'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/HTMLElement
    href: /dom/HTMLElement
  return_type:
    predicate: 'Returns an object of type  '
    value: ClientRect
    href: /dom/HTMLElement
standardization_status: 'W3C Working Draft'
summary: 'Returns a ClientRect object that encloses a group of text rectangles. '
tags:
  - API
  - Object
  - Methods
  - CSS
  - DOM
uri: dom/HTMLElement/getBoundingClientRect

---
## <span>Summary</span>

Returns a ClientRect object that encloses a group of text rectangles.

Method of [dom/HTMLElement](/dom/HTMLElement)[dom/HTMLElement](/dom/HTMLElement)

## <span>Syntax</span>

``` js
var rect = object.getBoundingClientRect();
```

## <span>Return Value</span>

Returns an object of type ClientRectClientRect

**[ClientRect](/css/cssom/ClientRect)**

     top: Number
     left: Number
     right: Number
     bottom: Number
     width: Number
     height: Number

## <span>Examples</span>

This example uses the [**getClientRects**](/dom/HTMLElement/getClientRects) and **getBoundingClientRect** methods to highlight text lines in an object.

``` html
<HEAD>
<SCRIPT>
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
</SCRIPT>
</HEAD>
<BODY ID="idBody">
<DIV ID="oID_1" onclick="Highlight(this)"
    onkeydown="Highlight(this)">
A large block of text should go here. Click this
block of text multiple times to see each line
highlight with every click of the mouse button.
Once each line has been highlighted, the process
begins again starting with the first line.
</DIV>
<DIV STYLE="position:absolute; left:5; top:400;
z-index:-1; background-color:yellow; display:none"
ID="idYellow"></DIV>
<DIV STYLE="position:absolute; left:5; top:400;
z-index:-1; background-color:beige; display:none"
ID="idBeige"></DIV>
</BODY>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/rectselection.htm)

This example uses the [**ClientRect**](/css/cssom/ClientRect) collection with the [**getClientRects**](/dom/HTMLElement/getClientRects) and **getBoundingClientRect** methods to determine the position of the text rectangle within an element. In each line, the left-justified text does not extend to the right margin of the box that contains the text. Using the collection, you can determine the coordinates of the rectangle that surrounds only the content in each line. The example code reads these rectangle coordinates and instructs the ball to move over the text only, and not to the end of the line.

``` html
<HEAD>
<SCRIPT>
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
</SCRIPT>
</HEAD>
<BODY ID="bodyid" onload="LoadDone()"
    onresize="End();LoadDone();" onunload="End()">
<P STYLE="text-align:center">
<B>The quick brown fox jumps over the lazy dog.</B>
</P>
<DIV ID="obj" STYLE="position:absolute">
<IMG ID="im" SRC="/workshop/graphics/dot.png"
    BORDER=0 HEIGHT=16 WIDTH=16>
</DIV>
</BODY>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/rectdemo.htm)

## <span>Usage</span>

     The returned value is a ClientRect object which is the union of the rectangles returned by getClientRects() for the element, i.e., the CSS border-boxes associated with the element. It contains read-only left, top, right, and bottom properties describing the border-box, in pixels, with the top-left relative to the top-left of the viewport.

Essentially, the browser calculates all rectangles (see below getClientRects()), and getBoundingClientRect() returns the lowest (top, left) or highest (bottom, right) values found.

The amount of scrolling that has been done of the viewport area (or any other scrollable element) is taken into account when computing the bounding rectangle. This means that the top and left property change their values as soon as the scrolling position changes (so their values are relative to the viewport and not absolute). If this is not the desired behaviour just add the current scrolling position to the top and left property (via window.scrollX and window.scrollY) to get constant values independent from the current scrolling position.

## <span>Notes</span>

### <span>Compatibility notes</span>

Internet Explorer 8 and below - **getBoundingClientRect** returns a proprietary `TextRectangle` object. While it is similar to [ClientRect](/css/cssom/ClientRect), it does not have `height` or `width` properties and furthermore cannot have any additional properties (including `height` and `width`) added to it.

## <span>Related specifications</span>

[CSSOM View Module](http://www.w3.org/TR/cssom-view/#the-getclientrects-and-getboundingclientrect-methods)
:   Working Draft
