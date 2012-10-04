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
|Description=This example uses the '''onmouseover''' event to apply a new style to an object.
|LiveURL=
|Code=
&lt;p 
	onmouseover{{=}}"this.style.color{{=}}'red'" 
    onmouseout{{=}}"this.style.color{{=}}'black'"&gt;
    	Move the mouse pointer over this text to change its color. Move the pointer off the text 
        to change the color back.
&lt;/p&gt;
}}
{{Single_Example
|Description=This example shows how to change the value of a text area in response to mouse events.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onmouseoverEX.htm
|Code=
&lt;p&gt;Move the mouse pointer into the text area to fire the onmouseover event. Move 
it out to clear the text.
&lt;textarea name{{=}}"txtMouseTrack" 
    onmouseover{{=}}"this.value{{=}}'onmouseover fired'" 
    onmouseout{{=}}"this.value{{=}}''"&gt;
&lt;/textarea&gt;&lt;/p&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
The event occurs when the user moves the mouse pointer into the object, and it does not repeat unless the user moves the mouse pointer out of the object and then back into it.
Initiates any action associated with this event.
To invoke this event, do one of the following:
*Move the mouse pointer into an object.

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
*<code>[[dom/events/mouseout|onmouseout]]</code>
*<code>[[dom/events/mouseup|onmouseup]]</code>
*<code>[[dom/events/mspointerhover|onmspointerhover]]</code>
*<code>[[dom/events/mspointerover|onmspointerover]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}