{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Event
|Interface=dom/Event
|Target=dom/Element
|Default_action=
|Content=
|Event_applies_to=dom/Event
|Synchronous=No
|Bubbles=No
|Cancelable=No
}}
{{Topics|Events}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example uses the '''onbeforeunload''' event to ask users whether they want to remain on the current document or navigate to a new URL. When the user clicks on the hyperlink or attempts to close the window, the '''onbeforeunload''' event fires on the '''body''' and a dialog box displays. If the user chooses '''OK''', the document navigates to the new URL (www.microsoft.com) or closes the window; if the user chooses '''Cancel''', the document remains the same.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onbeforeunload.htm
|Code=
&lt;HTML&gt;
&lt;head&gt;
&lt;script&gt;
function closeIt()
{
  return "Any string value here forces a dialog box to \n" + 
         "appear before closing the window.";
}
window.onbeforeunload {{=}} closeIt;
&lt;/script&gt;
&lt;/head&gt;
&lt;body&gt;
  &lt;a href{{=}}"http://www.microsoft.com"&gt;Click here to navigate to 
      www.microsoft.com&lt;/a&gt;
&lt;/body&gt;
&lt;/html&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
When a string is assigned to the '''returnValue''' property of '''window'''.'''event''', a dialog box appears that gives users the option to stay on the current document and retain the string that was assigned to it. The default statement that appears in the dialog box, "<code>Are you sure you want to navigate away from this page? ... Press OK to continue, or Cancel to stay on the current page.</code>", cannot be removed or altered.

====onbeforeunload in Metro style apps using JavaScript====
In Metro style apps using JavaScript,  the '''returnValue''' property of '''window'''.'''event'''  is always ignored and '''onunload''' will fire immediately.  No dialog is shown to the user and the navigation can't be cancelled. Note that, in most cases, the app should never navigate its top-level document. Metro style apps using JavaScript should use '''oncheckpoint''' event to determine when they need to save state information.

====General info====
This event signals that the document is about to be unloaded.
To invoke this event, do one of the following:
*Close the current window.
*Navigate to another location by entering a new address or selecting a Favorite.
*Click an [[html/elements/a|'''anchor''']] that refers to another document.
*Invoke the [[html/elements/a|'''anchor''']].[[dom/methods/click|'''click''']] method.
*Invoke the [[dom/Document|'''Document''']].[[dom/methods/write|'''write''']] method.
*Invoke the [[dom/Document|'''Document''']].[[dom/methods/close (document)|'''close''']] method.
*Invoke the '''window'''.[[dom/methods/close|'''close''']] method.
*Invoke the '''window'''.[[dom/methods/navigate|'''navigate''']] or '''NavigateAndFind''' method.
*Invoke the [[dom/location|'''location''']].[[dom/methods/replace|'''replace''']] method.
*Invoke the [[dom/location|'''location''']].[[dom/methods/reload|'''reload''']] method.
*Specify a new value for the [[dom/location|'''location''']].[[dom/properties/href|'''href''']] property.
*Submit a '''form''' to the address specified in the [[html/attributes/action|'''ACTION''']] attribute via the '''INPUT type{{=}}submit''' control, or invoke the '''form'''.[[dom/methods/submit|'''submit''']] method.
*Invoke the '''window'''.[[dom/methods/open|'''open''']] method, providing the possible value '''_self''' for the window name.
*Invoke the [[dom/Document|'''Document''']].[[dom/methods/open (document)|'''open''']] method.
*Click the Back, Forward, Refresh, or Home button.

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
*<code>body</code>
*<code>frameSet</code>
*<code>window</code>
*<code>Reference</code>
*<code>[[dom/events/load|onload]]</code>
*<code>[[dom/events/unload|onunload]]</code>
*<code>Conceptual</code>
*<code>Introduction to Data Binding</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}