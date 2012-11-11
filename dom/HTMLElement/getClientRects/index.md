{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|The returned value is a collection of ClientRect objects, one for each CSS border box associated with the element. Each ClientRect object contains read-only left, top, right and bottom properties describing the border box, in pixels, with the top-left relative to the top-left of the viewport. For tables with captions, the caption is included even though it's outside the border box of the table.}}
{{API_Object_Method
|Parameters=
|Method_applies_to=dom/HTMLElement
|Example_object_name=element
|Return_value_name=rectList
|Javascript_data_type=ClientRectList
|Return_value_description='''ClientRectList'''

'''ClientRect'''
  '''top''': Number
  '''left''': Number
  '''right''': Number
  '''bottom''': Number
  '''height''': Number
  '''width''': Number
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the '''getClientRects''' and [[dom/methods/getBoundingClientRect|'''getBoundingClientRect''']] methods to highlight text lines in an object.
|Code=&lt;HEAD&gt;
&lt;SCRIPT&gt;
var rcts;
var keyCount{{=}}0;
function Highlight(obj) {            
    rcts {{=}} obj.getClientRects();
    rctLength{{=}} rcts.length;
    if (keyCount &gt; rctLength-1) {
        idBeige.style.display{{=}}"none";
        keyCount {{=}} 0
    }
    // set the rendering properties for the yellow DIV
    cdRight {{=}} rcts[keyCount].right + idBody.scrollLeft;
    cdLeft {{=}} rcts[keyCount].left + idBody.scrollLeft;
    cdTop {{=}} rcts[keyCount].top + idBody.scrollTop;
    cdBottom {{=}} rcts[keyCount].bottom + idBody.scrollTop;
    idYellow.style.top {{=}} cdTop;
    idYellow.style.width {{=}} (cdRight-cdLeft) - 5;
    idYellow.style.display {{=}} 'inline';
    // set the rendering properties for the beige DIV
    bndRight {{=}} obj.getBoundingClientRect().right +
	    idBody.scrollLeft;
    bndLeft {{=}} obj.getBoundingClientRect().left +
	    idBody.scrollLeft;
    bndTop {{=}} obj.getBoundingClientRect().top +
	    idBody.scrollTop;
    idBeige.style.top {{=}} bndTop;
    idBeige.style.width {{=}} (bndRight-bndLeft) - 5;
    idBeige.style.height {{=}} cdTop - bndTop;
    if (keyCount&gt;0){
        idBeige.style.display {{=}} 'inline';
    }
    keyCount++;
}
&lt;/SCRIPT&gt;
&lt;/HEAD&gt;
&lt;BODY ID{{=}}"idBody"&gt;
&lt;DIV ID{{=}}"oID_1" onclick{{=}}"Highlight(this)"
    onkeydown{{=}}"Highlight(this)"&gt;
A large block of text should go here. Click this
block of text multiple times to see each line
highlight with every click of the mouse button.
Once each line has been highlighted, the process
begins again starting with the first line.
&lt;/DIV&gt;
&lt;DIV STYLE{{=}}"position:absolute; left:5; top:400;
z-index:-1; background-color:yellow; display:none"
ID{{=}}"idYellow"&gt;&lt;/DIV&gt;
&lt;DIV STYLE{{=}}"position:absolute; left:5; top:400;
z-index:-1; background-color:beige; display:none"
ID{{=}}"idBeige"&gt;&lt;/DIV&gt;
&lt;/BODY&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/rectselection.htm
}}{{Single Example
|Language=HTML
|Description=This example uses the [[dom/TextRectangle|'''TextRectangle''']] collection with the '''getClientRects''' and [[dom/methods/getBoundingClientRect|'''getBoundingClientRect''']] methods to determine the position of the text rectangle within an element. In each line, the left-justified text does not extend to the right margin of the box that contains the text. Using the collection, you can determine the coordinates of the rectangle that surrounds only the content in each line. The example code reads these rectangle coordinates and instructs the ball to move over the text only, and not to the end of the line.
|Code=&lt;HEAD&gt;
&lt;SCRIPT&gt;
var timid {{=}} -1;
var timoID_2 {{=}} -1;
var nLine;
var nPosInLine;
var oRcts;
var nDivLen;
var nEraser;
function LoadDone() {
    oTextRange {{=}} document.body.createTextRange();              
    // Get bounding rect of the range
    oRcts {{=}} oTextRange.getClientRects();
    nLine {{=}} 0;
    oBndRct {{=}} obj.getBoundingClientRect();
    nDivLen {{=}} oBndRct.right - oBndRct.left + 1;    
    MoveTo();
}
function MoveTo() {
    if (nLine &gt;{{=}} oRcts.length) {
	    nLine {{=}} 0;
	}
    obj.style.top {{=}} oRcts[nLine].top;
    nPosInLine {{=}} oRcts[nLine].left;
    nEraser {{=}} 0;
    timoID_2 {{=}} setInterval("MoveToInLine()",60);    
}
function MoveToInLine() {
    if (nPosInLine &gt;{{=}} oRcts[nLine].right - nDivLen) {
        clearInterval(timoID_2);
        timoID_2 {{=}} -1;
        obj.style.left {{=}} oRcts[nLine].right - nDivLen;
        nLine++;
        timid {{=}} setTimeout("MoveTo()", 100);
        return;
    }
    if (nEraser {{=}}{{=}} 0) {
	    nEraser {{=}} 1;
	}
    else {
	    nEraser {{=}} 0;
	}
	im.src {{=}} "/workshop/graphics/dot.png";
    obj.style.left {{=}} nPosInLine;
    nPosInLine +{{=}} 3;
}
function End() {
    if(timid !{{=}} -1) {
	    clearInterval(timid);
        timid {{=}} -1;
	}
    if(timoID_2 !{{=}} -1) {
	    clearInterval(timoID_2);
        timoID_2 {{=}} -1;
	}
}
&lt;/SCRIPT&gt;
&lt;/HEAD&gt;
&lt;BODY ID{{=}}"bodyid" onload{{=}}"LoadDone()"
    onresize{{=}}"End();LoadDone();" onunload{{=}}"End()"&gt;
&lt;P STYLE{{=}}"text-align:center"&gt;
&lt;B&gt;The quick brown fox jumps over the lazy dog.&lt;/B&gt;
&lt;/P&gt;
&lt;DIV ID{{=}}"obj" STYLE{{=}}"position:absolute"&gt;
&lt;IMG ID{{=}}"im" SRC{{=}}"/workshop/graphics/dot.png"
    BORDER{{=}}0 HEIGHT{{=}}16 WIDTH{{=}}16&gt;
&lt;/DIV&gt;
&lt;/BODY&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/rectdemo.htm
}}
}}
{{Notes_Section
|Usage=Originally, Microsoft intended this method to return a TextRectangle object for each line of text. However, the CSSOM working draft specifies that it returns a ClientRect for each border box. For an inline element, the two definitions are the same. But for a block element, Mozilla will return only a single rectangle.

The amount of scrolling that has been done of the viewport area (or any other scrollable element) is taken into account when computing the rectangles.

The returned rectangles do not include the bounds of any child elements that might happen to overflow.

For HTML AREA elements, SVG elements that do not render anything themselves, display:none elements, and generally any elements that are not directly rendered, an empty list is returned.

Rectangles are returned even for CSS boxes that have empty border-boxes. The left, top, right and bottom coordinates can still be meaningful.

Fractional pixel offsets are possible.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSSOM View Module
|URL=http://www.w3.org/TR/cssom-view/#dom-range-getclientrects
|Status=Working Draft
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=4
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=3
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=8
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=10.10
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=CSS Layout, CSSOM
}}
{{Topics|CSS, DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/DOM/element.getClientRects
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}