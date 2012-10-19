{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Event
|Interface=dom/objects/Event
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
|Description=This example shows how to fire the '''onlosecapture''' event. When the user clicks the mouse, the [[dom/methods/releaseCapture|'''releaseCapture''']] method is invoked and subsequently fires the '''onlosecapture''' event.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onlosecaptureEX.htm
|Code=
&lt;BODY onload{{=}}"divOwnCapture.setCapture()"
    onclick{{=}}"divOwnCapture.releaseCapture();"&gt;
&lt;DIV ID{{=}}divOwnCapture
    onmousemove{{=}}"txtWriteLocation.value{{=}}event.clientX 
		+ event.clientY";
    onlosecapture{{=}}"alert(event.srcElement.id 
		+ ' lost mouse capture.')"&gt;
&lt;P&gt;Mouse capture has been set to this gray division (DIV) at
   load time using the setCapture method. The text area will track
   the mousemove event anywhere in the document.&lt;BR&gt;&lt;BR&gt;
&lt;TEXTAREA ID{{=}}txtWriteLocation COLS{{=}}2&gt;&lt;/TEXTAREA&gt;
&lt;/DIV&gt;
&lt;HR&gt;
&lt;DIV ID{{=}}divNoCapture&gt;
&lt;P&gt;Click anywhere on the document to invoke the releaseCapture 
   method, whereby the onlosecapture event will fire.&lt;/P&gt;
&lt;/DIV&gt;
&lt;/BODY&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
Sends the event notification to the object that is losing the mouse capture.
To invoke this event, do one of the following:
*Set mouse capture to a different object.
*Change the active window so that the current document using mouse capture loses focus.
*Invoke the [[dom/methods/releaseCapture|'''releaseCapture''']] method on the [[dom/document|'''document''']] or object.

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

|Import_Notes=
===Syntax===
===Standards information===
There are no standards that apply here.

===Event handler parameters===
;''pEvtObj'' [in]:Type: '''<b>IHTMLEventObj'''</b>

}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[html/elements/a|a]]</code>
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
*<code>custom</code>
*<code>dd</code>
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
*<code>hn</code>
*<code>hr</code>
*<code>i</code>
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
*<code>[[dom/methods/releaseCapture|releaseCapture]]</code>
*<code>[[dom/methods/setCapture|setCapture]]</code>
*<code>[[dom/methods/msSetPointerCapture|msSetPointerCapture]]</code>
*<code>[[dom/methods/msReleasePointerCapture|msReleasePointerCapture]]</code>
*<code>Conceptual</code>
*<code>About Mouse Capture</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}