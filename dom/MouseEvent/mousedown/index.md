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
|Description=This example shows how to determine the origin of the '''onmousedown''' event when event bubbling is used.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onmousedownEX.htm
|Code=
&lt;BODY onmousedown{{=}}"console.log(event.srcElement.tagName)"&gt;
&lt;TABLE BORDER{{=}}1&gt;
  &lt;TH&gt;Click the items below with your mouse.&lt;/TH&gt;
  &lt;TR&gt;&lt;TD&gt;&lt;BUTTON&gt;Click Me&lt;/BUTTON&gt;&lt;/TD&gt;&lt;/TR&gt;
  &lt;TR&gt;&lt;TD&gt;&lt;INPUT TYPE{{=}}text VALUE{{=}}"Click Me"&gt;&lt;/TD&gt;&lt;/TR&gt;
  &lt;TR&gt;&lt;TD&gt;&lt;SPAN&gt;Click Me&lt;/SPAN&gt;&lt;/TD&gt;&lt;/TR&gt;
&lt;/TABLE&gt;
&lt;P&gt;This code retrieves the tagName of the object on which
   the onmousedown event has fired.
&lt;/BODY&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
Use the '''button''' property to determine which mouse button is clicked.
Initiates actions associated with the event and with the object being clicked.
To invoke this event, do one of the following:
*Click a mouse button.

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
*<code>[[dom/events/mousemove|onmousemove]]</code>
*<code>[[dom/events/mouseout|onmouseout]]</code>
*<code>[[dom/events/mouseover|onmouseover]]</code>
*<code>[[dom/events/mouseup|onmouseup]]</code>
*<code>[[dom/events/mspointerdown|onmspointerdown]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}