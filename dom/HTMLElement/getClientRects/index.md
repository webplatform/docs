{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Method
|Parameters=
|Method_applies_to=dom/HTMLElement
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description='''IHTMLRectCollection'''

'''TextRectangle'''

'''top'''

'''left'''

'''right'''

'''bottom'''
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
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
|Import_Notes====Syntax===
===Standards information===
There are no standards that apply here.
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=CSS Layout, CSSOM
}}
{{Topics|CSS, DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}