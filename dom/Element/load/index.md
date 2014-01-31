{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{Event
|Event_applies_to=dom/Element
|Synchronous=No
|Bubbles=No
|Target=dom/Element
|Cancelable=No
|Interface=dom/Element
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following example shows how to declare an '''onload''' event for a document that is designed to work with  multiple browsers and earlier versions of Internet Explorer.
|Code=&lt;!doctype html&gt;
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
}}
}}
{{Notes_Section
|Notes====Remarks===
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
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}25320 HTML 4.01 Specification], Section 18.2.3


===Event handler parameters===
;''pEvtObj'' [in]:Type: '''<b>IHTMLEventObj'''</b>
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
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}