{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=needs summary, spec, and compat
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
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
|Description=This example shows how to fire the '''onlosecapture''' event. When the user clicks the mouse, the [[dom/Document/releaseCapture|'''releaseCapture''']] method is invoked and subsequently fires the '''onlosecapture''' event.
|Code=&lt;BODY onload{{=}}"divOwnCapture.setCapture()"
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
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onlosecaptureEX.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
Sends the event notification to the object that is losing the mouse capture.
To invoke this event, do one of the following:
*Set mouse capture to a different object.
*Change the active window so that the current document using mouse capture loses focus.
*Invoke the [[dom/Document/releaseCapture|'''releaseCapture''']] method on the [[dom/Document|'''Document''']] or object.

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
|Import_Notes====Syntax===
===Standards information===
There are no standards that apply here.

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