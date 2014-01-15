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
|Interface=dom/Element
|Target=dom/Element
|Default_action=
|Synchronous=No
|Bubbles=No
|Cancelable=No
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example shows how to use the '''onunload''' event to run script when the window object has been unloaded.
|Code=&lt;head&gt;
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
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onunloadEX.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
If you call '''window'''.[[dom/Window/open|'''open''']] from this event, the Pop-up Blocker feature in Microsoft Internet Explorer 6 prevents the pop-up window from appearing.
Removes the object or document from the browser window.
To invoke this event, do one of the following:
*Close the current window.
*Navigate to another location by entering a new address or selecting a Favorite.
*Click the Back, Forward, Refresh, or Home button.
*Click an [[html/elements/a|'''anchor''']] that refers the browser to another document.
*Invoke the [[html/elements/a|'''anchor''']].[[dom/methods/click|'''click''']] method.
*Invoke the [[dom/Document|'''Document''']].[[dom/Document/write|'''write''']] method.
*Invoke the [[dom/Document|'''Document''']].[[dom/Document/open|'''open''']] method.
*Invoke the [[dom/Document|'''Document''']].[[dom/Document/close|'''close''']] method.
*Invoke the '''window'''.[[dom/Window/close|'''close''']] method.
*Invoke the '''window'''.[[dom/Window/open|'''open''']] method, providing the possible value '''_self''' for the window name.
*Invoke the [[dom/Location|'''location''']].[[dom/Location/replace|'''replace''']] method.
*Invoke the [[dom/location|'''Location''']].[[dom/Location/reload|'''reload''']] method.
*Specify a new value for the [[dom/Location|'''location''']].[[dom/Location/href|'''href''']] property.
*Submit a '''form''' to the address specified in the '''ACTION''' attribute via the '''INPUT type{{=}}submit''' control, or invoke the '''form'''.[[dom/HTMLFormElement/submit|'''submit''']] method.

For security reasons, the '''unload''' event does not open modeless dialog boxes, such as those created with the [[dom/Window/alert|'''alert''']] method or the [[dom/HTMLElement/showModelessDialog|'''showModelessDialog''']] method.  This changes affects webpages displayed in IE9 Standards mode or later document modes.
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
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>body</code>
*<code>frameSet</code>
*<code>window</code>
*<code>Reference</code>
*<code>Conceptual</code>
*<code>About the Pop-up Blocker</code>
}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}