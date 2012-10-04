{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=component|Data type=VARIANT|Description=A '''String''' that specifies how the object scrolls, using one of the following values.|Optional=}}
|Method_applies_to=dom/HTMLElement
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.

Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.


}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following example uses the '''doScroll''' method to scroll down when a button is clicked.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/doScrollEX.htm
|Code=
&lt;HEAD&gt;
&lt;SCRIPT&gt;  
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
&lt;/SCRIPT&gt;
&lt;/HEAD&gt;
&lt;BODY&gt;
&lt;BUTTON
   onclick{{=}}"scrollBehavior()"
   CLASS{{=}}"colorIt"
&gt;
Click to Scroll Page
&lt;/BUTTON&gt;
&lt;BR&gt;
&lt;HR&gt;
&lt;BUTTON
   onclick{{=}}"scrollBehavior1()"
   ondblclick{{=}}"scrollBehavior2()"
   CLASS{{=}}"colorIt"&gt;
   Click to Scroll Text Area
&lt;/BUTTON&gt;&lt;BR&gt;&lt;BR&gt;
&lt;TEXTAREA ID{{=}}txtScrollMe CLASS{{=}}"colorIt"&gt;
    This text area scrolls down	when
	the "Click to Scroll the Text 
	Area" button is clicked. The doScroll
	method scrolls it as if the down 
	arrow component of the scroll bar
	had been clicked. Double-click the 
	button to scroll down a whole page.
&lt;/BODY&gt;
}}
{{Single_Example
|Description=The following example uses the '''doScroll''' method to scroll down a text area in one-second intervals.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/doScrollEX1.htm
|Code=
&lt;HEAD&gt;
&lt;SCRIPT&gt;
var iTimer;
function timeIt()
{
iTimer {{=}} setInterval("scrollIt()", 1000);
}
function scrollIt()
{
oScrollMe.doScroll("down");
}
&lt;/SCRIPT&gt;
&lt;/HEAD&gt;
&lt;BODY onload{{=}}"timeIt()"&gt;
&lt;DIV ID{{=}}oScrollMe STYLE{{=}}"width:200px;height:75px;overflow:scroll"&gt;
&lt;/DIV&gt;
&lt;/BODY&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
As of Windows Internet Explorer 9, this method is supported only for webpages displayed in IE5 (Quirks) mode.  For webpages displayed in standards mode (preferred), use the [[dom/properties/scrollLeft|'''scrollLeft''']] and [[dom/properties/scrollTop|'''scrollTop''']] properties.
The '''doScroll''' method is available on all objects, regardless of whether they support scrollbars.
Cascading Style Sheets (CSS) allow you to scroll on all objects through the [[css/properties/overflow|'''overflow''']] property.
When the content of an element changes and causes scroll bars to display, the '''doScroll''' method might not work correctly immediately following the content update. When this happens, you can use the [[dom/methods/setTimeout|'''setTimeout''']] method to enable the browser to recognize the dynamic changes that affect scrolling.
|Import_Notes=
===Syntax===
===Standards information===
There are no standards that apply here.

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
*<code>base</code>
*<code>baseFont</code>
*<code>bdo</code>
*<code>bgSound</code>
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
*<code>comment</code>
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
*<code>frameSet</code>
*<code>head</code>
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
*<code>link</code>
*<code>listing</code>
*<code>map</code>
*<code>marquee</code>
*<code>menu</code>
*<code>[[html/elements/nextID|nextID]]</code>
*<code>noBR</code>
*<code>noFrames</code>
*<code>noScript</code>
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
*<code>script</code>
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
*<code>title</code>
*<code>tr</code>
*<code>tt</code>
*<code>u</code>
*<code>ul</code>
*<code>var</code>
*<code>wbr</code>
*<code>xml</code>
*<code>xmp</code>
*<code>Reference</code>
*<code>[[dom/methods/componentFromPoint|componentFromPoint]]</code>
*<code>[[dom/events/scroll|onscroll]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}