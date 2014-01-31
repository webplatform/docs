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
|Description=This example demonstrates how to use the '''onreset''' event for a '''form''' object. Reset the form by clicking the first or second button.  The only difference between the two buttons is that the second button invokes the [[dom/HTMLFormElement/reset|'''reset''']] method and the first button is of '''input type{{=}}reset'''. When either button is pressed the '''form''' is reset, resulting in the '''onreset''' event call on the '''form''' object. The '''onreset''' event calls an event handler which in turn adds the text <code>Resetting form.</code> to the text area below.
|Code=&lt;HTML&gt;
&lt;HEAD&gt;
&lt;SCRIPT&gt;
function doReset(){
    oTextArea1.innerText +{{=}} "Resetting form.  ";
}
&lt;/SCRIPT&gt;
&lt;/HEAD&gt;
&lt;BODY&gt;
&lt;FORM name{{=}}"form1" onreset{{=}}"doReset();"
    &lt;B&gt;Form&lt;/B&gt;&lt;BR&gt;
    style{{=}}"border:2px solid #cccccc; background:#EEEEEE; padding:10px; "&gt;
    &lt;b&gt;Enter some text:&lt;/b&gt;
    &lt;INPUT type{{=}}"text" name{{=}}"oText1" value{{=}}""&gt;&lt;BR&gt;&lt;BR&gt;
    &lt;INPUT TYPE{{=}}"reset" value{{=}}"Input type{{=}}reset"/&gt;
    &lt;BUTTON onclick{{=}}"form.reset();"&gt;form.reset()&lt;/BUTTON&gt;
&lt;/FORM&gt;
&lt;B&gt;Form status&lt;/B&gt;&lt;BR&gt;
&lt;SPAN id{{=}}"oTextArea1" &gt;&lt;/SPAN&gt;
&lt;BR&gt;&lt;BR&gt;
&lt;BUTTON onclick{{=}}"location.reload(true);"&gt;Refresh Page&lt;/BUTTON&gt;
&lt;/BODY&gt;
&lt;/HTML&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onreset.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
Executes associated code.
To invoke this event, do one of the following:
*Click an '''input type{{=}}reset''' button.
*Invoke the [[dom/HTMLFormElement/reset|'''reset''']] method.

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