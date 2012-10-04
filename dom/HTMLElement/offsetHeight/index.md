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
|Description=This example adjusts the size of a clock's readout to fit the current width and height of the document body.
|LiveURL=
|Code=
&lt;HTML&gt;
&lt;HEAD&gt;
&lt;TITLE&gt;A Simple Clock&lt;/TITLE&gt;
&lt;SCRIPT LANGUAGE{{=}}"JScript"&gt;
function startClock()
{
    window.setInterval("Clock_Tick()", 1000);
    Clock_Tick();
}

var iRatio {{=}} 4;
function Clock_Tick()
{
    var dToday {{=}} Date();
    var sTime {{=}} dToday.substring(11,19);
    var iDocHeight {{=}} document.body.offsetHeight;
    var iDocWidth {{=}} document.body.offsetWidth;

    if ((iDocHeight*iRatio)&gt;iDocWidth)
        iDocHeight {{=}} iDocWidth / iRatio;
    document.all.MyTime.innerText {{=}} sTime;
    document.all.MyTime.style.fontSize {{=}} iDocHeight;
}
&lt;/SCRIPT&gt;
&lt;/HEAD&gt;
&lt;BODY onload{{=}}"startClock()"&gt;
&lt;P ID{{=}}"MyTime"&gt;&amp;nbsp;&lt;/P&gt;
&lt;/BODY&gt;
&lt;/HTML&gt;
}}
{{Single_Example
|Description=This example uses the '''offsetHeight''' property and the [[dom/properties/clientHeight|'''clientHeight''']] property to show different ways of measuring the object size.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/offsetHeight.htm
|Code=
&lt;DIV ID{{=}}oDiv STYLE{{=}}"overflow:scroll; width:200; height:100"&gt; . . . &lt;/DIV&gt;
&lt;BUTTON onclick{{=}}"alert(oDiv.clientHeight)"&gt;client height&lt;/BUTTON&gt;
&lt;BUTTON onclick{{=}}"alert(oDiv.offsetHeight)"&gt;offset height&lt;/BUTTON&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
You can determine the location, width, and height of an object by using a combination of the [[dom/properties/offsetLeft|'''offsetLeft''']], [[dom/properties/offsetTop|'''offsetTop''']], '''offsetHeight''', and [[dom/properties/offsetWidth|'''offsetWidth''']] properties. These numeric properties specify the physical coordinates and dimensions of the object relative to the object's offset parent.
For more information about how to access the dimension and location of elements on the page through the Dynamic HTML (DHTML) Document Object Model (DOM), see Measuring Element Dimension and Location with CSSOM in Internet Explorer 9.
To comply with the [http://go.microsoft.com/fwlink/p/?linkid{{=}}203774 Cascading Style Sheets, Level 1 (CSS1)] box model, Microsoft Internet Explorer 6 and later calculate the height of objects differently when you use the [[html/elements/!DOCTYPE|!DOCTYPE]] declaration in your document to switch on standards-compliant mode.  This difference may affect the value of the '''offsetHeight''' property. When standards-compliant mode is switched on, the [[css/properties/height|'''height''']] property specifies the distance between the top and bottom edges of the bounding box that surrounds the object's content. When standards-compliant mode is not switched on, and with earlier versions of Windows Internet Explorer, the '''height''' property also includes the [[css/properties/border|'''border''']] and [[css/properties/padding|'''padding''']] belts that surround the object's bounding box. For more information, see CSS Enhancements in Internet Explorer 6.
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
*<code>article</code>
*<code>aside</code>
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
*<code>figcaption</code>
*<code>figure</code>
*<code>font</code>
*<code>footer</code>
*<code>form</code>
*<code>frame</code>
*<code>frameSet</code>
*<code>head</code>
*<code>header</code>
*<code>hgroup</code>
*<code>hn</code>
*<code>hr</code>
*<code>html</code>
*<code>i</code>
*<code>iframe</code>
*<code>img</code>
*<code>input type{{=}}button</code>
*<code>input type{{=}}checkbox</code>
*<code>input type{{=}}file</code>
*<code>input type{{=}}hidden</code>
*<code>input type{{=}}image</code>
*<code>input type{{=}}password</code>
*<code>input type{{=}}radio</code>
*<code>input type{{=}}reset</code>
*<code>input type{{=}}submit</code>
*<code>input type{{=}}text</code>
*<code>ins</code>
*<code>isIndex</code>
*<code>kbd</code>
*<code>label</code>
*<code>legend</code>
*<code>li</code>
*<code>listing</code>
*<code>map</code>
*<code>mark</code>
*<code>marquee</code>
*<code>menu</code>
*<code>nav</code>
*<code>[[html/elements/nextID|nextID]]</code>
*<code>noBR</code>
*<code>object</code>
*<code>ol</code>
*<code>optGroup</code>
*<code>option</code>
*<code>p</code>
*<code>plainText</code>
*<code>pre</code>
*<code>q</code>
*<code>rt</code>
*<code>ruby</code>
*<code>s</code>
*<code>samp</code>
*<code>section</code>
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
*<code>tFoot</code>
*<code>th</code>
*<code>tHead</code>
*<code>tr</code>
*<code>tt</code>
*<code>u</code>
*<code>ul</code>
*<code>var</code>
*<code>xmp</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}