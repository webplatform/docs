{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=summary, examples best practices, compatibility, standards, clean-up of MSDN sections
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=component
|Data type=VARIANT
|Description=A '''String''' that specifies how the object scrolls, using one of the following values.
|Optional=No
}}
|Method_applies_to=dom/HTMLElement
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.

Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following example uses the '''doScroll''' method to scroll down when a button is clicked.
|Code=&lt;HEAD&gt;
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
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/doScrollEX.htm
}}{{Single Example
|Description=The following example uses the '''doScroll''' method to scroll down a text area in one-second intervals.
|Code=&lt;HEAD&gt;
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
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/doScrollEX1.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
As of Windows Internet Explorer 9, this method is supported only for webpages displayed in IE5 (Quirks) mode.  For webpages displayed in standards mode (preferred), use the [[dom/HTMLElement/scrollLeft|'''scrollLeft''']] and [[dom/HTMLElement/scrollTop|'''scrollTop''']] properties.
The '''doScroll''' method is available on all objects, regardless of whether they support scrollbars.
Cascading Style Sheets (CSS) allow you to scroll on all objects through the [[css/properties/overflow|'''overflow''']] property.
When the content of an element changes and causes scroll bars to display, the '''doScroll''' method might not work correctly immediately following the content update. When this happens, you can use the [[dom/Window/setTimeout|'''setTimeout''']] method to enable the browser to recognize the dynamic changes that affect scrolling.
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
{{See_Also_Section}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}