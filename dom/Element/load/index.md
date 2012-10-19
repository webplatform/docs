{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Event
|Interface=dom/objects/UIEvent
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
|Description=The following example shows how to declare an '''onload''' event for a document that is designed to work with  multiple browsers and earlier versions of Internet Explorer.
|LiveURL=
|Code=
&lt;!doctype html&gt;
&lt;head&gt;
  &lt;title&gt;Load Event Sample&lt;/title&gt;
  &lt;script type{{=}}"text/javascript"&gt;
  function doLoad() {
     alert( "The load event is executing" );
  }
  if ( window.addEventListener ) { 
     window.addEventListener( "load", doLoad, false );
  }
  else 
     if ( window.attachEvent ) { 
        window.attachEvent( "onload", doLoad );
  } else 
        if ( window.onLoad ) {
           window.onload {{=}} doLoad;
  }
  &lt;/script&gt;
&lt;/head&gt;
&lt;body&gt;
  &lt;h1&gt;Load Event Sample&lt;/h1&gt;
  &lt;p&gt;This sample demonstrates how to execute 
     an event while the document is loading.&lt;/p&gt;
&lt;/body&gt;
&lt;/html&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
The client loads applications, embedded objects, and images as soon as it encounters the '''applet''', '''embed''', and '''img''' objects during parsing. Consequently, the '''onload''' event for these objects occurs before the client parses any subsequent objects. To ensure that an event handler receives the '''onload''' event for these objects, place the '''script''' object that defines the event handler before the object and use the '''onload''' attribute in the object to set the handler.
The '''onload''' attribute of the '''body''' object sets an '''onload''' event handler for the '''window'''. This technique of calling the window '''onload''' event through the '''body''' object is overridden by any other means of invoking the window '''onload''' event, provided the handlers are in the same script language.
Loads the object for which the event is specified.
To invoke this event, do one of the following:
*Open a document to invoke this event for the document or any object within it.

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
*<code>[[svg/elements/svg|SVGSVGElement]]</code>
*<code>Reference</code>
*<code>[[dom/events/readystatechange|onreadystatechange]]</code>
*<code>[[dom/events/unload|onunload]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}