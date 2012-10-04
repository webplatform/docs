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
|Description=This example shows how to use the '''onunload''' event to run script when the window object has been unloaded.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onunloadEX.htm
|Code=
&lt;head&gt;
&lt;script type{{=}}"text/javascript" for{{=}}"window" event{{=}}"onunload"&gt;
    alert("The onunload event fired for the window object.");
&lt;/script&gt;
&lt;script type{{=}}"text/javascript"&gt;
    function fnRelocate()
    {
    location.href{{=}}"/workshop/samples/author/dhtml/refs/onunloadEX_target.htm";
    }
&lt;/script&gt;
&lt;/head&gt;
&lt;body&gt;
&lt;input type{{=}}"button" value{{=}}"Go To Page 2" onclick{{=}}"fnRelocate()"&gt;
&lt;/body&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
If you call '''window'''.[[dom/methods/open|'''open''']] from this event, the Pop-up Blocker feature in Microsoft Internet Explorer 6 prevents the pop-up window from appearing.
Removes the object or document from the browser window.
To invoke this event, do one of the following:
*Close the current window.
*Navigate to another location by entering a new address or selecting a Favorite.
*Click the Back, Forward, Refresh, or Home button.
*Click an [[html/elements/a|'''anchor''']] that refers the browser to another document.
*Invoke the [[html/elements/a|'''anchor''']].[[dom/methods/click|'''click''']] method.
*Invoke the [[dom/document|'''document''']].[[dom/methods/write|'''write''']] method.
*Invoke the [[dom/document|'''document''']].[[dom/methods/open (document)|'''open''']] method.
*Invoke the [[dom/document|'''document''']].[[dom/methods/close (document)|'''close''']] method.
*Invoke the '''window'''.[[dom/methods/close|'''close''']] method.
*Invoke the '''window'''.[[dom/methods/open|'''open''']] method, providing the possible value '''_self''' for the window name.
*Invoke the '''window'''.[[dom/methods/navigate|'''navigate''']] or '''NavigateAndFind''' method.
*Invoke the [[dom/location|'''location''']].[[dom/methods/replace|'''replace''']] method.
*Invoke the [[dom/location|'''location''']].[[dom/methods/reload|'''reload''']] method.
*Specify a new value for the [[dom/location|'''location''']].[[dom/properties/href|'''href''']] property.
*Submit a '''form''' to the address specified in the [[html/attributes/action|'''ACTION''']] attribute via the '''INPUT type{{=}}submit''' control, or invoke the '''form'''.[[dom/methods/submit|'''submit''']] method.

For security reasons, the '''unload''' event does not open modeless dialog boxes, such as those created with the [[dom/methods/alert|'''alert''']] method or the [[dom/methods/showModelessDialog|'''showModelessDialog''']] method.  This changes affects webpages displayed in IE9 Standards mode or later document modes.
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
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}25320 HTML 4.01 Specification], Section 18.2.3


===Event handler parameters===
;''pEvtObj'' [in]:Type: '''<b>IHTMLEventObj'''</b>

}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>body</code>
*<code>frameSet</code>
*<code>window</code>
*<code>Reference</code>
*<code>[[dom/events/load|onload]]</code>
*<code>[[dom/events/beforeunload|onbeforeunload]]</code>
*<code>Conceptual</code>
*<code>About the Pop-up Blocker</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}