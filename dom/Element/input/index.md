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
{{Topics|Event}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following script queries the event [[dom/properties/target|'''target''']] as the text in a '''textArea''' is changed.
|LiveURL=
|Code=
&lt;script type{{=}}"text/javascript"&gt;
function handleInput(ev) {
    alert(ev.target.value);
}
window.onload {{=}} function() {
    document.getElementById('myTextArea').addEventListener('input',handleInput,false);
}
&lt;/script&gt;
&lt;textarea id{{=}}"myTextArea"&gt;Edit this text.&lt;/textarea&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
You can use the '''oninput''' to detect when the contents of a '''textArea''', '''input type{{=}}text''', or '''input type{{=}}password''' have changed. This event occurs immediately after modification, unlike the [[dom/events/change|'''onchange''']] event, which occurs when the element loses focus.
To invoke this event, do one of the following:
*Enter some text into a form field.
*Cut, delete, or paste content.
*Navigate to another document.

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
*'''HTMLElementEvents4'''

|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML]


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
*<code>base</code>
*<code>baseFont</code>
*<code>bdo</code>
*<code>bgSound</code>
*<code>big</code>
*<code>body</code>
*<code>blockQuote</code>
*<code>br</code>
*<code>button</code>
*<code>[[canvas/objects/canvas|canvas]]</code>
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
*<code>[[dom/document|document]]</code>
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
*<code>[[html/elements/media|media]]</code>
*<code>menu</code>
*<code>meta</code>
*<code>[[html/elements/nextID|nextID]]</code>
*<code>noBR</code>
*<code>noFrames</code>
*<code>noScript</code>
*<code>object</code>
*<code>ol</code>
*<code>optGroup</code>
*<code>option</code>
*<code>p</code>
*<code>param</code>
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
*<code>source</code>
*<code>span</code>
*<code>strike</code>
*<code>strong</code>
*<code>style</code>
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
*<code>video</code>
*<code>window</code>
*<code>xmp</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}