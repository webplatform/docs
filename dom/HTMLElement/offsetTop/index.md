{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=dom/HTMLElement
|Read_only=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example uses the '''offsetTop''' property to determine whether an object is in the user's view.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/offsetTop.htm
|Code=
&lt;html&gt;

&lt;head&gt;
&lt;script type{{=}}"text/javascript"&gt;
function isinView(oObject)
{
    var oParent {{=}} oObject.offsetParent; 
    var iOffsetTop {{=}} oObject.offsetTop;
    var iClientHeight {{=}} oParent.clientHeight;
    if (iOffsetTop &gt; iClientHeight) {
        alert("Special Text not in view. Expand Window to put Text in View.");
    }
    else{
         alert("Special Text in View!");
    }
}
&lt;/script&gt;
&lt;/head&gt;

&lt;body onload{{=}}"window.resizeTo(430,250)" onclick{{=}}"isinView(oID_1)" scroll{{=}}"NO"&gt;

&lt;div style{{=}}"position: absolute; left: 20px"&gt;
    Click anywhere in window to see if special text is in view.&lt;/div&gt;
&lt;div id{{=}}"oID_1" style{{=}}"position: absolute; 
    left: 50px; 
    top: 300px; 
    width: 280px; 
    color: silver; 
    font-size: large; 
    font-weight: bold; 
    background-color: aqua; 
    font-family: Arial"&gt;
    Here&amp;#39;s some special text &lt;/div&gt;

&lt;/body&gt;

&lt;/html&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
You can determine the location, width, and height of an object by using a combination of the [[dom/properties/offsetLeft|'''offsetLeft''']], '''offsetTop''', [[dom/properties/offsetHeight|'''offsetHeight''']], and [[dom/properties/offsetWidth|'''offsetWidth''']] properties. These numeric properties specify the physical coordinates and dimensions of the object relative to the object's offset parent.
You can determine the location, width, and height of an object by using a combination of the [[dom/properties/offsetLeft|'''offsetLeft''']], '''offsetTop''', [[dom/properties/offsetHeight|'''offsetHeight''']], and [[dom/properties/offsetWidth|'''offsetWidth''']] properties. These numeric properties specify the physical coordinates and dimensions of the object relative to the object's offset parent.
For more information about how to access the dimension and location of objects on the page through the Dynamic HTML (DHTML) Document Object Model (DOM), see Measuring Element Dimension and Location with CSSOM in Internet Explorer 9.
|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[html/elements/a|a]]</code>
*<code>abbr</code>
*<code>[[html/elements/acronym|acronym]]</code>
*<code>address</code>
*<code>applet</code>
*<code>area</code>
*<code>b</code>
*<code>bdo</code>
*<code>big</code>
*<code>blockQuote</code>
*<code>body</code>
*<code>br</code>
*<code>button</code>
*<code>caption</code>
*<code>center</code>
*<code>cite</code>
*<code>code</code>
*<code>col</code>
*<code>colGroup</code>
*<code>custom</code>
*<code>dd</code>
*<code>del</code>
*<code>dfn</code>
*<code>dir</code>
*<code>div</code>
*<code>dl</code>
*<code>dt</code>
*<code>em</code>
*<code>embed</code>
*<code>fieldSet</code>
*<code>font</code>
*<code>form</code>
*<code>frame</code>
*<code>hn</code>
*<code>hr</code>
*<code>i</code>
*<code>iframe</code>
*<code>img</code>
*<code>input type{{=}}button</code>
*<code>input type{{=}}checkbox</code>
*<code>input type{{=}}file</code>
*<code>input type{{=}}image</code>
*<code>input type{{=}}password</code>
*<code>input type{{=}}radio</code>
*<code>input type{{=}}reset</code>
*<code>input type{{=}}submit</code>
*<code>input type{{=}}text</code>
*<code>ins</code>
*<code>kbd</code>
*<code>label</code>
*<code>legend</code>
*<code>li</code>
*<code>listing</code>
*<code>map</code>
*<code>marquee</code>
*<code>menu</code>
*<code>noBR</code>
*<code>object</code>
*<code>ol</code>
*<code>option</code>
*<code>p</code>
*<code>plainText</code>
*<code>pre</code>
*<code>q</code>
*<code>rt</code>
*<code>ruby</code>
*<code>s</code>
*<code>samp</code>
*<code>select</code>
*<code>small</code>
*<code>span</code>
*<code>strike</code>
*<code>strong</code>
*<code>sub</code>
*<code>sup</code>
*<code>[[html/elements/table|table]]</code>
*<code>tBody</code>
*<code>td</code>
*<code>textArea</code>
*<code>[[dom/traversal/TextRange|TextRange]]</code>
*<code>tFoot</code>
*<code>th</code>
*<code>tHead</code>
*<code>tr</code>
*<code>tt</code>
*<code>u</code>
*<code>ul</code>
*<code>var</code>
*<code>xmp</code>
*<code>Reference</code>
*<code>boundingHeight</code>
*<code>boundingLeft</code>
*<code>boundingTop</code>
*<code>boundingWidth</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}