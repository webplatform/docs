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
|Description=This example uses the '''onreadystatechange''' event to invoke a function when the [[dom/Element/readyState|'''readyState''']] is complete.
|Code=document.onreadystatechange{{=}}fnStartInit;
function fnStartInit()
{
   if (document.readyState{{=}}{{=}}"complete")
   {
      // Finish initialization.
   }
}
}}
}}
{{Notes_Section
|Notes====Remarks===
You can use the [[dom/Element/readyState|'''readyState''']] property to query the current state of the element when the '''onreadystatechange''' event fires.
All elements expose an '''onreadystatechange''' event. The following objects always fire the event because they load data: '''applet''', [[dom/Document|'''Document''']], '''frame''', '''frameSet''', '''iframe''', '''img''', '''link''', '''object''', '''script''', and '''xml''' elements. Other objects will only fire the '''onreadystatechange''' event when a DHTML Behavior is attached.
When working with behaviors, wait for the '''onreadystatechange''' event to fire and verify that the '''readyState''' property of the element is set to '''complete''' to ensure that the behavior is completely downloaded and applied to the element. Until the '''onreadystatechange''' event fires, if you use any of the behavior-defined members before attaching the behavior to the element, a scripting error can result, indicating that the object does not support that particular property or method.
Signals the ready state of the document.
To invoke this event, do one of the following:
*Change the ready state.

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