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
|Event_applies_to=dom/Document
|Interface=dom/Document
|Target=dom/Element
|Default_action=
|Synchronous=No
|Bubbles=No
|Cancelable=No
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example uses the '''onstop''' event to stop a function from executing in a continuous cycle. The [[dom/Window/setInterval|'''setInterval''']] method is used to execute script every millisecond. If the user clicks the '''Stop''' button, the [[dom/Window/clearInterval|'''clearInterval''']] method removes the interval and the script is no longer executed.
|Code=document.onstop{{=}}fnTrapStop;
window.onload{{=}}fnInit;
var oInterval;
function fnInit(){
   oInterval{{=}}window.setInterval("fnCycle()",1);
}
function fnCycle(){
   // Do something
}
function fnTrapStop(){
   window.clearInterval(oInterval);
}
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''onstop''' event fires after the [[dom/Event/beforeunload|'''beforeunload''']] event, and before the [[dom/Element/unload|'''unload''']] event.
Initiates any action associated with this event.
To invoke this event, do one of the following:
*Click the Stop button.
*Leave the document.

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
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}