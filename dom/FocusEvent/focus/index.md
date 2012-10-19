{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Event
|Interface=dom/objects/FocusEvent
|Target=dom/Element
|Default_action=
|Content=
|Event_applies_to=dom/Element
|Synchronous=No
|Bubbles=No
|Cancelable=No
}}
{{Topics|Events}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example uses the '''onfocus''' event to make '''INPUT_text''' and '''label''' objects more accessible. When the '''INPUT_text''' object has focus, the '''onfocus''' event fires and the [[css/properties/background-color|'''backgroundColor''']], [[css/properties/font-size|'''fontSize''']], and [[css/properties/font-weight|'''fontWeight''']] properties are changed to give the control more prominence.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onfocusEX.htm
|Code=
...
&lt;style type{{=}}"text/css"&gt;
.normal {
	background-color: white;
	color: black;
	font-weight: normal;
	font-size: 8pt;
	font-family: Arial;
}
.accessible {
	background-color: silver;
	font-weight: bold;
	font-size: 10pt;
}
&lt;/style&gt;
&lt;script type{{=}}"text/javascript"&gt;
function fnSetStyle(){
   event.srcElement.className{{=}}"accessible";
   var oWorkLabel{{=}}eval(event.srcElement.id + "_label");
   oWorkLabel.className{{=}}"accessible";
}
&lt;/script&gt;
&lt;label for{{=}}"oInput" class{{=}}"normal" id{{=}}"oInput_label"&gt;Enter some text&lt;/label&gt;
&lt;input type{{=}}"text" class{{=}}"normal" onfocus{{=}}"fnSetStyle()" id{{=}}"oInput"&gt; 
...
}}}}
{{Notes_Section
|Notes=
===Remarks===
'''Note'''  Using the [[dom/methods/setActive|'''setActive''']] method has no effect on document focus. Using the [[dom/methods/focus|'''focus''']] method on an individual element causes the element to gain focus and become the active element.
When one object loses activation and another object becomes the [[dom/properties/activeElement|'''activeElement''']], the '''onfocus''' event fires on the object becoming the '''activeElement''' only after the [[dom/events/blur|'''onblur''']] event fires on the object losing activation. Use the focus events to determine when to prepare an object to receive input from the user.
Elements cannot receive focus until the document is finished loading.
For Microsoft Internet Explorer 5.5 and later, focus on a [[dom/document|'''document''']], and the [[dom/properties/activeElement|'''active element''']] of a '''document''' can be managed separately. The synchronous events [[dom/events/activate|'''onactivate''']] and [[dom/events/deactivate|'''ondeactivate''']] provide better control for managing activation changes.
As of Microsoft Internet Explorer 5, elebrowserments retain focus within the current  history when the user returns to a page. To avoid firing the '''onfocus''' event unintentionally for an element when the document loads, invoke the [[dom/methods/focus|'''focus''']] method on another element.
As of Internet Explorer 5, you can force elements that do not implicitly receive focus to receive focus by adding them to the document tabbing order using the [[html/attributes/tabIndex|'''TABINDEX''']] attribute.
Sets focus to an object.
To invoke this event, do one of the following:
*Click an object.
*Use keyboard navigation.
*Invoke the [[dom/methods/focus|'''focus''']] method.
*Invoke the [[dom/methods/setActive|'''setActive''']] method.

The ''pEvtObj'' parameter is required for the following interfaces:
*'''HTMLAnchorEvents2'''
*'''HTMLAreaEvents2'''
*'''HTMLButtonElementEvents2'''
*'''HTMLControlElementEvents2'''
*'''HTMLDocumentEvents2'''
*'''HTMLElementEvents2'''
*'''HTMLFormElementEvents2'''
*'''HTMLImgEvents2'''
*'''HTMLFrameSiteEvents2'''
*'''HTMLInputFileElementEvents2'''
*'''HTMLInputImageEvents2'''
*'''HTMLInputTextElementEvents2'''
*'''HTMLLabelEvents2'''
*'''HTMLLinkElementEvents2'''
*'''HTMLMapEvents2'''
*'''HTMLMarqueeElementEvents2'''
*'''HTMLObjectElementEvents2'''
*'''HTMLOptionButtonElementEvents2'''
*'''HTMLScriptEvents2'''
*'''HTMLSelectElementEvents2'''
*'''HTMLStyleElementEvents2'''
*'''HTMLTableEvents2'''
*'''HTMLTextContainerEvents2'''
*'''HTMLWindowEvents2'''
*'''HTMLDocumentEvents4'''

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
*<code>button</code>
*<code>[[canvas/objects/canvas|canvas]]</code>
*<code>caption</code>
*<code>center</code>
*<code>cite</code>
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
*<code>frame</code>
*<code>frameSet</code>
*<code>hn</code>
*<code>hr</code>
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
*<code>marquee</code>
*<code>[[html/elements/media|media]]</code>
*<code>menu</code>
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
*<code>Reference</code>
*<code>[[dom/methods/blur|blur]]</code>
*<code>[[dom/methods/focus|focus]]</code>
*<code>[[dom/events/focusin|onfocusin]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}