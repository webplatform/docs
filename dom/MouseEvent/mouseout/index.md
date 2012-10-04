{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Event
|Interface=dom/objects/MouseEvent
|Target=dom/Element
|Default_action=
|Content=
|Event_applies_to=dom/Element
|Synchronous=No
|Bubbles=No
|Cancelable=No
}}
{{Topics|Event}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example uses the '''onmouseout''' event to apply a new style to an object.
|LiveURL=
|Code=
&lt;body&gt;
&lt;p onmouseout{{=}}"this.style.color{{=}}'black';" 
    onmouseover{{=}}"this.style.color{{=}}'red';"&gt;
Move the mouse pointer over this text to change its color. 
Move the pointer off the text to change the color back.
&lt;/p&gt;
&lt;/body&gt;
}}
{{Single_Example
|Description=This example shows how to swap images on mouse events.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onmouseoutEX.htm
|Code=
&lt;head&gt;
&lt;script type{{=}}"text/javascript"&gt;
function flipImage(url)
{
    if (window.event.srcElement.tagName {{=}}{{=}} "img" )
	{
		window.event.srcElement.src {{=}} url;
    }
}
&lt;/script&gt;
&lt;/head&gt;
&lt;body&gt;
&lt;p&gt;Move the mouse over the image to see it switch.&lt;/p&gt;
&lt;p&gt;
&lt;img src{{=}}"/workshop/graphics/prop_ro.png" 
    onmouseover{{=}}"flipImage('/workshop/graphics/prop_rw.png');" 
    onmouseout{{=}}"flipImage('/workshop/graphics/prop_ro.png');"&gt;
&lt;/p&gt;
&lt;/body&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
When the user moves the mouse over an object, one [[dom/events/mouseover|'''onmouseover''']] event occurs, followed by one or more [[dom/events/mousemove|'''onmousemove''']] events as the user moves the mouse pointer within the object. One '''onmouseout''' event occurs when the user moves the mouse pointer out of the object.
Initiates any action associated with this event.
To invoke this event, do one of the following:
*Move the mouse pointer out of an object.

|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}25320 HTML 4.01 Specification], Section 18.2.3


===Event handler parameters===
;''pEvtObj'' [in]:Type: '''<b>IHTMLEventObj'''</b>

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
*<code>audio</code>
*<code>b</code>
*<code>bdo</code>
*<code>big</code>
*<code>blockQuote</code>
*<code>body</code>
*<code>button</code>
*<code>[[canvas/objects/canvas|canvas]]</code>
*<code>caption</code>
*<code>center</code>
*<code>cite</code>
*<code>code</code>
*<code>custom</code>
*<code>dd</code>
*<code>del</code>
*<code>dfn</code>
*<code>dir</code>
*<code>div</code>
*<code>dl</code>
*<code>[[dom/document|document]]</code>
*<code>dt</code>
*<code>em</code>
*<code>embed</code>
*<code>fieldSet</code>
*<code>font</code>
*<code>form</code>
*<code>hn</code>
*<code>hr</code>
*<code>i</code>
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
*<code>source</code>
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
*<code>video</code>
*<code>window</code>
*<code>xmp</code>
*<code>[[svg/elements/svg|SVGSVGElement]]</code>
*<code>Reference</code>
*<code>[[dom/events/mousewheel|onmousewheel]]</code>
*<code>[[dom/events/mousedown|onmousedown]]</code>
*<code>[[dom/events/mousemove|onmousemove]]</code>
*<code>[[dom/events/mouseover|onmouseover]]</code>
*<code>[[dom/events/mouseup|onmouseup]]</code>
*<code>[[dom/events/mspointerout|onmspointerout]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}